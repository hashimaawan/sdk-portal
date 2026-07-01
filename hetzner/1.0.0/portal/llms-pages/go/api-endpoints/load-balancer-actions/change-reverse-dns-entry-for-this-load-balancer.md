# Change Reverse DNS Entry for This Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjByZXZlcnNlJTI1MjBETlMlMjUyMGVudHJ5JTI1MjBmb3IlMjUyMHRoaXMlMjUyMExvYWQlMjUyMEJhbGFuY2Vy

Changes the hostname that will appear when getting the hostname belonging to the public IPs (IPv4 and IPv6) of this Load Balancer.

Floating IPs assigned to the Server are not affected by this.

:information_source: **Note** This endpoint does not require authentication.

```go
ChangeReverseDnsEntryForThisLoadBalancer(
    ctx context.Context,
    id int,
    body *models.ChangeLoadbalancerDnsPtrRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`*models.ChangeLoadbalancerDnsPtrRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/change-loadbalancer-dns-ptr-request.md) | Body, Optional | Select the IP address for which to change the DNS entry by passing `ip`. It can be either IPv4 or IPv6. The target hostname is set by passing `dns_ptr`. |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.ChangeLoadbalancerDnsPtrRequest{
    DnsPtr:                models.ToPointer("lb1.example.com"),
    Ip:                    "1.2.3.4",
}

apiResponse, err := loadBalancerActionsApi.ChangeReverseDnsEntryForThisLoadBalancer(ctx, id, &body)
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
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "load_balancer"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



