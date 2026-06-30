# Forbidden

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkZvcmJpZGRlbg

*This model accepts additional fields of type Any.*


# Class Name

`ForbiddenException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
try:
    # make the API call
except ForbiddenException as e:
    print(e)
except ApiException as e:
    print(e)
```



