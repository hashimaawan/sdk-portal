# Change Reverse DNS Entry for This Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjByZXZlcnNlJTI1MjBETlMlMjUyMGVudHJ5JTI1MjBmb3IlMjUyMHRoaXMlMjUyMExvYWQlMjUyMEJhbGFuY2Vy

Changes the hostname that will appear when getting the hostname belonging to the public IPs (IPv4 and IPv6) of this Load Balancer.

Floating IPs assigned to the Server are not affected by this.

:information_source: **Note** This endpoint does not require authentication.

```csharp
ChangeReverseDNSEntryForThisLoadBalancerAsync(
    int id,
    Models.ChangeLoadbalancerDnsPtrRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`ChangeLoadbalancerDnsPtrRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/change-loadbalancer-dns-ptr-request.md) | Body, Optional | Select the IP address for which to change the DNS entry by passing `ip`. It can be either IPv4 or IPv6. The target hostname is set by passing `dns_ptr`. |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`Task<Models.ActionResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md)


# Example Usage

```csharp
int id = 112;
ChangeLoadbalancerDnsPtrRequest body = new ChangeLoadbalancerDnsPtrRequest
{
    DnsPtr = "lb1.example.com",
    Ip = "1.2.3.4",
};

try
{
    ActionResponse result = await loadBalancerActionsController.ChangeReverseDNSEntryForThisLoadBalancerAsync(
        id,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
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



