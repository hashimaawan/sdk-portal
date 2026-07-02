# Floating I Ps Action Post

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRmZsb2F0aW5nSVBzQWN0aW9uX3Bvc3Q

To initiate an action on a floating IP send a POST request to
`/v2/floating_ips/$FLOATING_IP/actions`. In the JSON body to the request,
set the `type` attribute to on of the supported action types:

| Action     | Details
|------------|--------
| `assign`   | Assigns a floating IP to a Droplet
| `unassign` | Unassign a floating IP from a Droplet

```python
def floating_i_ps_action_post(self,
                             floating_ip,
                             body=None)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ip` | `str` | Template, Required | A floating IP address. |
| `body` | [BaseType](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/base-type.md) \| [V2 Floating Ips Actions Request](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-floating-ips-actions-request.md) \| None | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response will be an object with a key called `action`. The value of this will be an object that contains the standard floating IP action attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2FloatingIpsActionsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-floating-ips-actions-response-1.md).


# Example Usage

```python
floating_ip = '45.55.96.47'

body = V2ReservedIpsActionsRequest(
    droplet_id=758604968,
    mtype='V2 Reserved Ips Actions Request'
)

result = floating_ip_actions_api.floating_i_ps_action_post(
    floating_ip,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



