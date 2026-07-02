# Droplet Actions Post by Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkRyb3BsZXQlMjUyMEFjdGlvbnMlMkZkcm9wbGV0QWN0aW9uc19wb3N0X2J5VGFn

Some actions can be performed in bulk on tagged Droplets. The actions can be
initiated by sending a POST to `/v2/droplets/actions?tag_name=$TAG_NAME` with
the action arguments.

Only a sub-set of action types are supported:

- `power_cycle`
- `power_on`
- `power_off`
- `shutdown`
- `enable_ipv6`
- `enable_backups`
- `disable_backups`
- `snapshot`

```python
def droplet_actions_post_by_tag(self,
                               tag_name=None,
                               body=None)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tag_name` | `str` | Query, Optional | Used to filter Droplets by a specific tag. Can not be combined with `name`. |
| `body` | [V2 Droplets Actions Request](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-droplets-actions-request.md) \| [V2 Droplets Actions Request1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-droplets-actions-request-1.md) \| None | Body, Optional | This is a container for one-of cases. |


# Response Type

**201**: The response will be a JSON object with a key called `actions`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2DropletsActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-droplets-actions-response.md).


# Example Usage

```python
tag_name = 'env:prod'

body = V2DropletsActionsRequest(
    mtype=Type12.REBOOT
)

result = droplet_actions_api.droplet_actions_post_by_tag(
    tag_name=tag_name,
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



