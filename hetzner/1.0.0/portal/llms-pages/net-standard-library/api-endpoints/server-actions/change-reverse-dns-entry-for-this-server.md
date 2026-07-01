# Change Reverse DNS Entry for This Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkNoYW5nZSUyNTIwcmV2ZXJzZSUyNTIwRE5TJTI1MjBlbnRyeSUyNTIwZm9yJTI1MjB0aGlzJTI1MjBTZXJ2ZXI

Changes the hostname that will appear when getting the hostname belonging to the primary IPs (IPv4 and IPv6) of this Server.

Floating IPs assigned to the Server are not affected by this.

:information_source: **Note** This endpoint does not require authentication.

```csharp
ChangeReverseDnsEntryForThisServerAsync(
    int id,
    Models.ServersActionsChangeDnsPtrRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`ServersActionsChangeDnsPtrRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/servers-actions-change-dns-ptr-request.md) | Body, Optional | Select the IP address for which to change the DNS entry by passing `ip`. It can be either IPv4 or IPv6. The target hostname is set by passing `dns_ptr`. |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md).


# Example Usage

```csharp
int id = 112;
ServersActionsChangeDnsPtrRequest body = new ServersActionsChangeDnsPtrRequest
{
    DnsPtr = "server01.example.com",
    Ip = "1.2.3.4",
};

try
{
    ApiResponse<ActionResponse> result = await serverActionsApi.ChangeReverseDnsEntryForThisServerAsync(
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
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



