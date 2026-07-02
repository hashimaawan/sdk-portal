# Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk5hbWVzcGFjZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Namespace`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `api_host` | `str` | Optional | The namespace's API hostname. Each function in a namespace is provided an endpoint at the namespace's hostname. |
| `created_at` | `str` | Optional | UTC time string. |
| `key` | `str` | Optional | A random alpha numeric string. This key is used in conjunction with the namespace's UUID to authenticate<br>a user to use the namespace via `doctl`, DigitalOcean's official CLI. |
| `label` | `str` | Optional | The namespace's unique name. |
| `namespace` | `str` | Optional | A unique string format of UUID with a prefix fn-. |
| `region` | `str` | Optional | The namespace's datacenter region. |
| `updated_at` | `str` | Optional | UTC time string. |
| `uuid` | `str` | Optional | The namespace's Universally Unique Identifier. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.namespace import Namespace

namespace = Namespace(
    api_host='https://api_host.io',
    created_at='2022-09-14T04:16:45Z',
    key='d1zcd455h01mqjfs4s2eaewyejehi5f2uj4etqq3h7cera8iwkub6xg5of1wdde2',
    label='my namespace',
    namespace='fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
    region='nyc1',
    updated_at='2022-09-14T04:16:45Z',
    uuid='xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



