# V2 1 Clicks 401 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMDQwMSUyNTIwRXJyb3I

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V21Clicks401ErrorException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Required | A short identifier corresponding to the HTTP status code returned. For  example, the ID for a response returning a 404 status code would be "not_found." |
| `message` | `str` | Required | A message providing additional information about the error, including  details to help resolve it when possible. |
| `request_id` | `str` | Optional | Optionally, some endpoints may include a request ID that should be  provided when reporting bugs or opening support tickets to help  identify the issue. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
try:
    # make the API call
except V21Clicks401ErrorException as e:
    print(e)
except ApiException as e:
    print(e)
```



