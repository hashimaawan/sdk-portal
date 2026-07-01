# Change Alias I Ps of a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkNoYW5nZSUyNTIwYWxpYXMlMjUyMElQcyUyNTIwb2YlMjUyMGElMjUyME5ldHdvcms

Changes the alias IPs of an already attached Network. Note that the existing aliases for the specified Network will be replaced with these provided in the request body. So if you want to add an alias IP, you have to provide the existing ones from the Network plus the new alias IP in the request body.

:information_source: **Note** This endpoint does not require authentication.

```go
ChangeAliasIPsOfANetwork(
    ctx context.Context,
    id int,
    body *models.ServersActionsChangeAliasIpsRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`*models.ServersActionsChangeAliasIpsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/servers-actions-change-alias-ips-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.ServersActionsChangeAliasIpsRequest{
    AliasIps:              []string{
        "10.0.1.2",
    },
    Network:               4711,
}

apiResponse, err := serverActionsApi.ChangeAliasIPsOfANetwork(ctx, id, &body)
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
    "command": "change_alias_ips",
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



