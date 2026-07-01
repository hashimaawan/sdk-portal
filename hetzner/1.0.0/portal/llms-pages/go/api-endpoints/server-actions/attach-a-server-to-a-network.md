# Attach a Server to a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkF0dGFjaCUyNTIwYSUyNTIwU2VydmVyJTI1MjB0byUyNTIwYSUyNTIwTmV0d29yaw

Attaches a Server to a network. This will complement the fixed public Server interface by adding an additional ethernet interface to the Server which is connected to the specified network.

The Server will get an IP auto assigned from a subnet of type `server` in the same `network_zone`.

Using the `alias_ips` attribute you can also define one or more additional IPs to the Servers. Please note that you will have to configure these IPs by hand on your Server since only the primary IP will be given out by DHCP.

**Call specific error codes**

| Code                             | Description                                                           |
|----------------------------------|-----------------------------------------------------------------------|
| `server_already_attached`        | The server is already attached to the network                         |
| `ip_not_available`               | The provided Network IP is not available                              |
| `no_subnet_available`            | No Subnet or IP is available for the Server within the network        |
| `networks_overlap`               | The network IP range overlaps with one of the server networks         |

:information_source: **Note** This endpoint does not require authentication.

```go
AttachAServerToANetwork(
    ctx context.Context,
    id int,
    body *models.AttachToNetworkRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`*models.AttachToNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/attach-to-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.AttachToNetworkRequest{
    AliasIps:             []string{
        "10.0.1.2",
    },
    Ip:                   models.ToPointer("10.0.1.1"),
    Network:              4711,
}

apiResponse, err := serverActionsController.AttachAServerToANetwork(ctx, id, &body)
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
    "command": "attach_to_network",
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
      },
      {
        "id": 4711,
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



