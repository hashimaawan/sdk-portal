# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/python/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `msg` | `str` | Optional | HTTP Response Message |
| `response_id` | `str` | Optional | A unique ID paired with this response from the API. |
| `status` | `int` | Optional | HTTP Response Code |


# Example

```python
from giphyapi.models.meta import Meta

meta = Meta(
    msg='OK',
    response_id='57eea03c72381f86e05c35d2',
    status=200
)
```



