# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `registry` | `str` | Optional | The registry name. Must be left empty for the `DOCR` registry type. |
| `registry_type` | [`RegistryType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/registry-type.md) | Optional | - DOCKER_HUB: The DockerHub container registry type.<br>- DOCR: The DigitalOcean container registry type. |
| `repository` | `str` | Optional | The repository name. |
| `tag` | `str` | Optional | The repository tag. Defaults to `latest` if not provided.<br><br>**Default**: `"latest"` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.image import Image
from digitaloceanapi.models.registry_type import RegistryType

image = Image(
    registry='registry.hub.docker.com',
    registry_type=RegistryType.DOCR,
    repository='origin/master',
    tag='latest',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



