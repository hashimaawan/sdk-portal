# Repository 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlcG9zaXRvcnkx

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Repository1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `latest_manifest` | [`LatestManifest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/latest-manifest.md) | Optional | - |
| `manifest_count` | `int` | Optional | The number of manifests in the repository. |
| `name` | `str` | Optional | The name of the repository. |
| `registry_name` | `str` | Optional | The name of the container registry. |
| `tag_count` | `int` | Optional | The number of tags in the repository. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.blob import Blob
from digitaloceanapi.models.latest_manifest import LatestManifest
from digitaloceanapi.models.repository_1 import Repository1

repository_1 = Repository1(
    latest_manifest=LatestManifest(
        blobs=[
            Blob(
                compressed_size_bytes=12,
                digest='digest2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Blob(
                compressed_size_bytes=12,
                digest='digest2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Blob(
                compressed_size_bytes=12,
                digest='digest2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        compressed_size_bytes=154,
        digest='digest0',
        registry_name='registry_name4',
        repository='repository4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    manifest_count=1,
    name='repo-1',
    registry_name='example',
    tag_count=1,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



