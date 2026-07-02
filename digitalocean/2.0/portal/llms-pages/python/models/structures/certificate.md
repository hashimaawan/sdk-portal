# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the certificate was created. |
| `dns_names` | `List[str]` | Optional | An array of fully qualified domain names (FQDNs) for which the certificate was issued. |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference a certificate. |
| `name` | `str` | Optional | A unique human-readable name referring to a certificate. |
| `not_after` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents the certificate's expiration date. |
| `sha_1_fingerprint` | `str` | Optional, Read-only | A unique identifier generated from the SHA-1 fingerprint of the certificate. |
| `state` | [`State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/state.md) | Optional, Read-only | A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`. |
| `mtype` | [`Type4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.certificate import Certificate
from digitaloceanapi.models.state import State
from digitaloceanapi.models.type_4 import Type4

certificate = Certificate(
    created_at=dateutil.parser.parse('2017-02-08T16:02:37Z'),
    dns_names=[
        'www.example.com',
        'example.com'
    ],
    id='892071a0-bb95-49bc-8021-3afd67a210bf',
    name='web-cert-01',
    not_after=dateutil.parser.parse('2017-02-22T00:23:00Z'),
    sha_1_fingerprint='dfcc9f57d86bf58e321c2c6c31c7a971be244ac7',
    state=State.VERIFIED,
    mtype=Type4.LETS_ENCRYPT,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



