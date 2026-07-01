# Change IP Range of a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZDaGFuZ2UlMjUyMElQJTI1MjByYW5nZSUyNTIwb2YlMjUyMGElMjUyME5ldHdvcms

Changes the IP range of a Network. IP ranges can only be extended and never shrunk. You can only add IPs at the end of an existing IP range. This means that the IP part of your existing range must stay the same and you can only change its netmask.

For example if you have a range `10.0.0.0/16` you want to extend then your new range must also start with the IP `10.0.0.0`. Your CIDR netmask `/16` may change to a number that is smaller than `16` thereby increasing the IP range. So valid entries would be `10.0.0.0/15`, `10.0.0.0/14`, `10.0.0.0/13` and so on.

After changing the IP range you will have to adjust the routes on your connected Servers by either rebooting them or manually changing the routes to your private Network interface.

Note: if the Network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```go
ChangeIpRangeOfANetwork(
    ctx context.Context,
    id int,
    body *models.ChangeIpRangeRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Network |
| `body` | [`*models.ChangeIpRangeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/change-ip-range-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_ip_range` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.ChangeIpRangeRequest{
    IpRange:               "10.0.0.0/12",
}

apiResponse, err := networkActionsApi.ChangeIpRangeOfANetwork(ctx, id, &body)
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
    "command": "change_ip_range",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 4711,
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



