# V2 Tags 400 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjA0MDAlMjUyMEVycm9y

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2Tags400ErrorException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | `str` | Required | A message providing information about the error. |
| `messages` | `List[str]` | Optional | A list of error messages. |
| `root_causes` | `List[str]` | Required | A list of underlying causes for the error, including details to help  resolve it when possible. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
try:
    # make the API call
except V2Tags400ErrorException as e:
    print(e)
except ApiException as e:
    print(e)
```



