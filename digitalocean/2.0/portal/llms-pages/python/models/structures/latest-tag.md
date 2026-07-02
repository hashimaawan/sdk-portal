# Latest Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxhdGVzdFRhZw

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`LatestTag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `compressed_size_bytes` | `int` | Optional | The compressed size of the tag in bytes. |
| `manifest_digest` | `str` | Optional | The digest of the manifest associated with the tag. |
| `registry_name` | `str` | Optional | The name of the container registry. |
| `repository` | `str` | Optional | The name of the repository. |
| `size_bytes` | `int` | Optional | The uncompressed size of the tag in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `tag` | `str` | Optional | The name of the tag. |
| `updated_at` | `datetime` | Optional | The time the tag was last updated. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.latest_tag import LatestTag

latest_tag = LatestTag(
    compressed_size_bytes=2803255,
    manifest_digest='sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
    registry_name='example',
    repository='repo-1',
    size_bytes=5861888,
    tag='latest',
    updated_at=dateutil.parser.parse('2020-04-09T23:54:25Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



