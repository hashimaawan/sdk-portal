# V2 Registry Docker Credentials Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRG9ja2VyJTI1MjBDcmVkZW50aWFscyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2RegistryDockerCredentialsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auths` | [`Auths`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/auths.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.auths import Auths
from digitaloceanapi.models.registry_digitalocean_com import RegistryDigitaloceanCom
from digitaloceanapi.models.v_2_registry_docker_credentials_response import V2RegistryDockerCredentialsResponse

v_2_registry_docker_credentials_response = V2RegistryDockerCredentialsResponse(
    auths=Auths(
        registry_digitalocean_com=RegistryDigitaloceanCom(
            auth='auth0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



