# Unauthorized

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRlVuYXV0aG9yaXplZA

*This model accepts additional fields of type Any.*


# Class Name

`UnauthorizedException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
try:
    # make the API call
except UnauthorizedException as e:
    print(e)
except ApiException as e:
    print(e)
```



