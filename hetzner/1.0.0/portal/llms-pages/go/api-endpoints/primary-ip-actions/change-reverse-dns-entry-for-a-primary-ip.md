# Change Reverse DNS Entry for a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjByZXZlcnNlJTI1MjBETlMlMjUyMGVudHJ5JTI1MjBmb3IlMjUyMGElMjUyMFByaW1hcnklMjUyMElQ

Changes the hostname that will appear when getting the hostname belonging to this Primary IP.

:information_source: **Note** This endpoint does not require authentication.

```go
ChangeReverseDNSEntryForAPrimaryIP(
    ctx context.Context,
    id int,
    body *models.ChangeDNSPTRRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Primary IP |
| `body` | [`*models.ChangeDNSPTRRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/change-dnsptr-request.md) | Body, Optional | Select the IP address for which to change the DNS entry by passing `ip`. For a Primary IP of type `ipv4` this must exactly match the IP address of the Primary IP. For a Primary IP of type `ipv6` this must be a single IP within the IPv6 /64 range that belongs to this Primary IP.<br><br>The target hostname is set by passing `dns_ptr`. |


# Response Type

**201**: The `action` key contains the `change_dns_ptr` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.ChangeDNSPTRRequest{
    DnsPtr:               models.ToPointer("server02.example.com"),
    Ip:                   "1.2.3.4",
}

apiResponse, err := primaryIPActionsController.ChangeReverseDNSEntryForAPrimaryIP(ctx, id, &body)
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
    "command": "change_dns_ptr",
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
        "type": "primary_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



