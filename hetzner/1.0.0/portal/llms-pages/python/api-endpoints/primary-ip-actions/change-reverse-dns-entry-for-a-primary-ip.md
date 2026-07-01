# Change Reverse DNS Entry for a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjByZXZlcnNlJTI1MjBETlMlMjUyMGVudHJ5JTI1MjBmb3IlMjUyMGElMjUyMFByaW1hcnklMjUyMElQ

Changes the hostname that will appear when getting the hostname belonging to this Primary IP.

:information_source: **Note** This endpoint does not require authentication.

```python
def change_reverse_dns_entry_for_a_primary_ip(self,
                                             id,
                                             body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Primary IP |
| `body` | [`ChangeDnsptrRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/change-dnsptr-request.md) | Body, Optional | Select the IP address for which to change the DNS entry by passing `ip`. For a Primary IP of type `ipv4` this must exactly match the IP address of the Primary IP. For a Primary IP of type `ipv6` this must be a single IP within the IPv6 /64 range that belongs to this Primary IP.<br><br>The target hostname is set by passing `dns_ptr`. |


# Response Type

**201**: The `action` key contains the `change_dns_ptr` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md).


# Example Usage

```python
id = 112

body = ChangeDnsptrRequest(
    dns_ptr='server02.example.com',
    ip='1.2.3.4'
)

result = primary_ip_actions_api.change_reverse_dns_entry_for_a_primary_ip(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
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



