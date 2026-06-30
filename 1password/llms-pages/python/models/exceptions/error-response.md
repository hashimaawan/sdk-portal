# Error Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkVycm9yUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`ErrorResponseException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | A message detailing the error |
| `status` | `int` | Optional | HTTP Status Code |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
try:
    # make the API call
except ErrorResponseException as e:
    print(e)
except ApiException as e:
    print(e)
```



