# V2 Registry Repositories V2 Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwUmVwb3NpdG9yaWVzVjIlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2RegistryRepositoriesV2Response`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `repositories` | [`List[Repository1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/repository-1.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.blob import Blob
from digitaloceanapi.models.latest_manifest import LatestManifest
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.repository_1 import Repository1
from digitaloceanapi.models.v_2_registry_repositories_v_2_response import V2RegistryRepositoriesV2Response

v_2_registry_repositories_v_2_response = V2RegistryRepositoriesV2Response(
    meta=Meta(
        total=5,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    repositories=[
        Repository1(
            latest_manifest=LatestManifest(
                blobs=[
                    Blob(
                        compressed_size_bytes=1471,
                        digest='sha256:14119a10abf4669e8cdbdff324a9f9605d99697215a0d21c360fe8dfa8471bab',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    Blob(
                        compressed_size_bytes=12,
                        digest='sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e',
                        additional_properties={
                            'compressed_size_byte': jsonpickle.decode('2814446')
                        }
                    ),
                    Blob(
                        compressed_size_bytes=528,
                        digest='sha256:69704ef328d05a9f806b6b8502915e6a0a4faa4d72018dc42343f511490daf8a',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                compressed_size_bytes=1972332,
                digest='sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
                registry_name='example',
                repository='repo-1',
                size_bytes=2816445,
                tags=[
                    'v1',
                    'v2'
                ],
                updated_at=dateutil.parser.parse('2021-04-09T23:54:25Z'),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            manifest_count=82,
            name='repo-1',
            registry_name='example',
            tag_count=57,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='https://api.digitalocean.com/v2/registry/example/repositoriesV2?page=5&per_page=1',
            next='https://api.digitalocean.com/v2/registry/example/repositoriesV2?page=2&page_token=JPZmZzZXQiOjB9&per_page=1',
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



