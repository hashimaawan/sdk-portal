# Create a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkNyZWF0ZSUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Creates a new Primary IP, optionally assigned to a Server.

If you want to create a Primary IP that is not assigned to a Server, you need to provide the `datacenter` key instead of `assignee_id`. This can be either the ID or the name of the Datacenter this Primary IP shall be created in.

Note that a Primary IP can only be assigned to a Server in the same Datacenter later on.

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `server_not_stopped`          | The specified server is running, but needs to be powered off  |
| `server_has_ipv4`             | The server already has an ipv4 address                        |
| `server_has_ipv6`             | The server already has an ipv6 address                        |

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<CreatePrimaryIPResponse> createAPrimaryIPAsync(
    final CreatePrimaryIPRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreatePrimaryIPRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/create-primary-ip-request.md) | Body, Optional | The `type` argument is required while `datacenter` and `assignee_id` are mutually exclusive. |


# Response Type

**201**: The `primary_ip` key contains the Primary IP that was just created

[`CreatePrimaryIPResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/create-primary-ip-response.md)


# Example Usage

```java
CreatePrimaryIPRequest body = new CreatePrimaryIPRequest.Builder(
    "server",
    "my-ip",
    Type51Enum.IPV4
)
.assigneeId(17)
.autoDelete(false)
.datacenter("fsn1-dc8")
.labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
.build();

primaryIPsController.createAPrimaryIPAsync(body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "create_primary_ip",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 17,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  },
  "primary_ip": {
    "assignee_id": 17,
    "assignee_type": "server",
    "auto_delete": true,
    "blocked": false,
    "created": "2016-01-30T23:50:00+00:00",
    "datacenter": {
      "description": "Falkenstein DC Park 8",
      "id": 42,
      "location": {
        "city": "Falkenstein",
        "country": "DE",
        "description": "Falkenstein DC Park 1",
        "id": 1,
        "latitude": 50.47612,
        "longitude": 12.370071,
        "name": "fsn1",
        "network_zone": "eu-central"
      },
      "name": "fsn1-dc8",
      "server_types": {
        "available": [
          1,
          2,
          3
        ],
        "available_for_migration": [
          1,
          2,
          3
        ],
        "supported": [
          1,
          2,
          3
        ]
      }
    },
    "dns_ptr": [
      {
        "dns_ptr": "server.example.com",
        "ip": "2001:db8::1"
      }
    ],
    "id": 42,
    "ip": "131.232.99.1",
    "labels": {
      "labelkey": "value"
    },
    "name": "my-ip",
    "protection": {
      "delete": false
    },
    "type": "ipv4"
  }
}
```



