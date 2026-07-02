# Configurations for External Logging

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25zJTI1MjBmb3IlMjUyMGV4dGVybmFsJTI1MjBsb2dnaW5nLg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ConfigurationsForExternalLogging`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datadog` | [`Datadog`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/datadog.md) | Optional | DataDog configuration. |
| `logtail` | [`Logtail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/logtail.md) | Optional | Logtail configuration. |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `2`, *Maximum Length*: `42`, *Pattern*: `^[A-Za-z0-9()\[\]'"][-A-Za-z0-9_. \/()\[\]]{0,40}[A-Za-z0-9()\[\]'"]$` |
| `papertrail` | [`Papertrail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/papertrail.md) | Optional | Papertrail configuration. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.configurations_for_external_logging import ConfigurationsForExternalLogging
from digitaloceanapi.models.datadog import Datadog
from digitaloceanapi.models.logtail import Logtail
from digitaloceanapi.models.papertrail import Papertrail

configurations_for_external_logging = ConfigurationsForExternalLogging(
    name='my_log_destination',
    datadog=Datadog(
        api_key='api_key2',
        endpoint='endpoint8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    logtail=Logtail(
        token='token4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    papertrail=Papertrail(
        endpoint='endpoint4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



