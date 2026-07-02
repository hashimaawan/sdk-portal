# Contains All Domains for the App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkNvbnRhaW5zJTI1MjBhbGwlMjUyMGRvbWFpbnMlMjUyMGZvciUyNTIwdGhlJTI1MjBhcHA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ContainsAllDomainsForTheApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_expires_at` | `datetime` | Optional, Read-only | - |
| `id` | `str` | Optional | - |
| `phase` | [`Phase1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/phase-1.md) | Optional | **Default**: `"UNKNOWN"` |
| `progress` | [`Progress1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/progress-1.md) | Optional | - |
| `rotate_validation_records` | `bool` | Optional, Read-only | - |
| `spec` | [`Domain`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/domain.md) | Optional | - |
| `validations` | [`List[ListOfTxtValidationRecord]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/list-of-txt-validation-record.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.contains_all_domains_for_the_app import ContainsAllDomainsForTheApp
from digitaloceanapi.models.phase_1 import Phase1
from digitaloceanapi.models.progress_1 import Progress1

contains_all_domains_for_the_app = ContainsAllDomainsForTheApp(
    certificate_expires_at=dateutil.parser.parse('2024-01-29T23:59:59Z'),
    id='4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
    phase=Phase1.ACTIVE,
    progress=Progress1(
        steps=[
            jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
            jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
            jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    rotate_validation_records=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



