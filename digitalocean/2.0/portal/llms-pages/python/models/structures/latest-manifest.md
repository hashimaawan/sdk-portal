# Latest Manifest

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxhdGVzdE1hbmlmZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`LatestManifest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blobs` | [`List[Blob]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/blob.md) | Optional | All blobs associated with this manifest |
| `compressed_size_bytes` | `int` | Optional | The compressed size of the manifest in bytes. |
| `digest` | `str` | Optional | The manifest digest |
| `registry_name` | `str` | Optional | The name of the container registry. |
| `repository` | `str` | Optional | The name of the repository. |
| `size_bytes` | `int` | Optional | The uncompressed size of the manifest in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `tags` | `List[str]` | Optional | All tags associated with this manifest |
| `updated_at` | `datetime` | Optional | The time the manifest was last updated. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.blob import Blob
from digitaloceanapi.models.latest_manifest import LatestManifest

latest_manifest = LatestManifest(
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
    compressed_size_bytes=2803255,
    digest='sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
    registry_name='example',
    repository='repo-1',
    size_bytes=5861888,
    tags=[
        'latest',
        'v1',
        'v2'
    ],
    updated_at=dateutil.parser.parse('2020-04-09T23:54:25Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



