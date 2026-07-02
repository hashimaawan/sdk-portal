# Cors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkNvcnM

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Cors`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_credentials` | `bool` | Optional | Whether browsers should expose the response to the client-side JavaScript code when the request’s credentials mode is include. This configures the `Access-Control-Allow-Credentials` header. |
| `allow_headers` | `List[str]` | Optional | The set of allowed HTTP request headers. This configures the `Access-Control-Allow-Headers` header. |
| `allow_methods` | `List[str]` | Optional | The set of allowed HTTP methods. This configures the `Access-Control-Allow-Methods` header. |
| `allow_origins` | [`List[AllowOrigin]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/allow-origin.md) | Optional | The set of allowed CORS origins. |
| `expose_headers` | `List[str]` | Optional | The set of HTTP response headers that browsers are allowed to access. This configures the `Access-Control-Expose-Headers` header. |
| `max_age` | `str` | Optional | An optional duration specifying how long browsers can cache the results of a preflight request. This configures the `Access-Control-Max-Age` header. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.allow_origin import AllowOrigin
from digitaloceanapi.models.cors import Cors

cors = Cors(
    allow_credentials=False,
    allow_headers=[
        'Content-Type',
        'X-Custom-Header'
    ],
    allow_methods=[
        'GET',
        'OPTIONS',
        'POST',
        'PUT',
        'PATCH',
        'DELETE'
    ],
    allow_origins=[
        AllowOrigin(
            exact='https://www.example.com',
            prefix='prefix6',
            regex='regex4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        AllowOrigin(
            exact='exact8',
            prefix='prefix6',
            regex='^.*example.com',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    expose_headers=[
        'Content-Encoding',
        'X-Custom-Header'
    ],
    max_age='5h30m',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



