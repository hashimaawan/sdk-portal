# Create a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZDcmVhdGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Creates a new Floating IP assigned to a Server. If you want to create a Floating IP that is not bound to a Server, you need to provide the `home_location` key instead of `server`. This can be either the ID or the name of the Location this IP shall be created in. Note that a Floating IP can be assigned to a Server in any Location later on. For optimal routing it is advised to use the Floating IP in the same Location it was created in.

:information_source: **Note** This endpoint does not require authentication.

```go
CreateAFloatingIP(
    ctx context.Context,
    body *models.CreateFloatingIPRequest) (
    models.ApiResponse[models.FloatingIpsResponse1],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`*models.CreateFloatingIPRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/create-floating-ip-request.md) | Body, Optional | The `type` argument is required while `home_location` and `server` are mutually exclusive. |


# Response Type

**201**: The `floating_ip` key in the reply contains the object that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.FloatingIpsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/floating-ips-response-1.md).


# Example Usage

```go
ctx := context.Background()

body := models.CreateFloatingIPRequest{
    Description:          models.ToPointer("Web Frontend"),
    HomeLocation:         models.ToPointer("fsn1"),
    Labels:               models.ToPointer(interface{}("[labelkey, value]")),
    Name:                 models.ToPointer("Web Frontend"),
    Server:               models.ToPointer(42),
    Type:                 models.Type17Enum_IPV4,
}

apiResponse, err := floatingIPsController.CreateAFloatingIP(ctx, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "create_floating_ip",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  },
  "floating_ip": {
    "blocked": false,
    "created": "2016-01-30T23:50:00+00:00",
    "description": "Web Frontend",
    "dns_ptr": [
      {
        "dns_ptr": "server.example.com",
        "ip": "2001:db8::1"
      }
    ],
    "home_location": {
      "city": "Falkenstein",
      "country": "DE",
      "description": "Falkenstein DC Park 1",
      "id": 1,
      "latitude": 50.47612,
      "longitude": 12.370071,
      "name": "fsn1",
      "network_zone": "eu-central"
    },
    "id": 4711,
    "ip": "131.232.99.1",
    "labels": {
      "env": "dev"
    },
    "name": "Web Frontend",
    "protection": {
      "delete": false
    },
    "server": 42,
    "type": "ipv4"
  }
}
```



