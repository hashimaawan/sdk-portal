# Change Reverse DNS Entry for a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkNoYW5nZSUyNTIwcmV2ZXJzZSUyNTIwRE5TJTI1MjBlbnRyeSUyNTIwZm9yJTI1MjBhJTI1MjBGbG9hdGluZyUyNTIwSVA

Changes the hostname that will appear when getting the hostname belonging to this Floating IP.

:information_source: **Note** This endpoint does not require authentication.

```python
def change_reverse_dns_entry_for_a_floating_ip(self,
                                              id,
                                              body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`ChangeDNSPTRRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/change-dnsptr-request.md) | Body, Optional | Select the IP address for which to change the DNS entry by passing `ip`. For a Floating IP of type `ipv4` this must exactly match the IP address of the Floating IP. For a Floating IP of type `ipv6` this must be a single IP within the IPv6 /64 range that belongs to this Floating IP.<br><br>The target hostname is set by passing `dns_ptr`. |


# Response Type

**201**: The `action` key contains the `change_dns_ptr` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

body = ChangeDNSPTRRequest(
    dns_ptr='server02.example.com',
    ip='1.2.3.4'
)

result = floating_ip_actions_controller.change_reverse_dns_entry_for_a_floating_ip(
    id,
    body=body
)
print(result)
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
        "type": "floating_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



