# Not Found

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRk5vdEZvdW5k

*This model accepts additional fields of type Any.*


# Class Name

`NotFoundException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
try:
    # make the API call
except NotFoundException as e:
    print(e)
except ApiException as e:
    print(e)
```



