# An App Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFuJTI1MjBhcHAlMjUyMGRlcGxveW1lbnQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`AnAppDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cause` | `str` | Optional | - |
| `cloned_from` | `str` | Optional | - |
| `created_at` | `datetime` | Optional | - |
| `functions` | [`List[FunctionsComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/functions-components-that-are-part-of-this-deployment.md) | Optional | - |
| `id` | `str` | Optional | - |
| `jobs` | [`List[JobComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/job-components-that-are-part-of-this-deployment.md) | Optional | - |
| `phase` | [`Phase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/phase.md) | Optional | **Default**: `"UNKNOWN"` |
| `phase_last_updated_at` | `datetime` | Optional | - |
| `progress` | [`Progress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/progress.md) | Optional | - |
| `services` | [`List[ServiceComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/service-components-that-are-part-of-this-deployment.md) | Optional | - |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `static_sites` | [`List[StaticSiteComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/static-site-components-that-are-part-of-this-deployment.md) | Optional | - |
| `tier_slug` | `str` | Optional, Read-only | - |
| `updated_at` | `datetime` | Optional | - |
| `workers` | [`List[WorkerComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/worker-components-that-are-part-of-this-deployment.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.an_app_deployment import AnAppDeployment
from digitaloceanapi.models.functions_components_that_are_part_of_this_deployment import FunctionsComponentsThatArePartOfThisDeployment
from digitaloceanapi.models.phase import Phase

an_app_deployment = AnAppDeployment(
    cause='commit 9a4df0b pushed to github/digitalocean/sample-golang',
    cloned_from='3aa4d20e-5527-4c00-b496-601fbd22520a',
    created_at=dateutil.parser.parse('2020-07-28T18:00:00Z'),
    functions=[
        FunctionsComponentsThatArePartOfThisDeployment(
            name='name4',
            namespace='namespace8',
            source_commit_hash='source_commit_hash4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    id='b6bdf840-2854-4f87-a36c-5f231c617c84',
    phase=Phase.ACTIVE,
    phase_last_updated_at=dateutil.parser.parse('0001-01-01T00:00:00Z'),
    tier_slug='basic',
    updated_at=dateutil.parser.parse('2020-07-28T18:00:00Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



