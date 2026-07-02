# Functions Delete Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkZ1bmN0aW9ucyUyRmZ1bmN0aW9uc19kZWxldGVfdHJpZ2dlcg

Deletes the given trigger.
To delete trigger, send a DELETE request to `/v2/functions/namespaces/$NAMESPACE_ID/triggers/$TRIGGER_NAME`.
A successful deletion returns a 204 response.

```python
def functions_delete_trigger(self,
                            namespace_id,
                            trigger_name)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namespace_id` | `str` | Template, Required | The ID of the namespace to be managed. |
| `trigger_name` | `str` | Template, Required | The name of the trigger to be managed. |


# Response Type

**204**: The action was successful and the response body is empty.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
namespace_id = 'fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx'

trigger_name = 'my trigger'

result = functions_api.functions_delete_trigger(
    namespace_id,
    trigger_name
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
| 404 | Bad Request. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



