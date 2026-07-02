# Repository

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlcG9zaXRvcnk

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Repository`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `latest_tag` | [`LatestTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/latest-tag.md) | Optional | - |
| `name` | `str` | Optional | The name of the repository. |
| `registry_name` | `str` | Optional | The name of the container registry. |
| `tag_count` | `int` | Optional | The number of tags in the repository. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.latest_tag import LatestTag
from digitaloceanapi.models.repository import Repository

repository = Repository(
    latest_tag=LatestTag(
        compressed_size_bytes=108,
        manifest_digest='manifest_digest2',
        registry_name='registry_name4',
        repository='repository4',
        size_bytes=226,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    name='repo-1',
    registry_name='example',
    tag_count=1,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



