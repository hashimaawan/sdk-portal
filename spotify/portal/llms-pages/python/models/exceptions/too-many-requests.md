# Too Many Requests

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRlRvb01hbnlSZXF1ZXN0cw

*This model accepts additional fields of type Any.*


# Class Name

`TooManyRequestsException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/error-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
try:
    # make the API call
except TooManyRequestsException as e:
    print(e)
except ApiException as e:
    print(e)
```



