# V2 Apps Rollback Validate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwVmFsaWRhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsRollbackValidateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/error.md) | Optional | - |
| `valid` | `bool` | Optional | Indicates whether the app can be rolled back to the specified deployment. |
| `warnings` | [`List[Warning]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/warning.md) | Optional | Contains a list of warnings that may cause the rollback to run under unideal circumstances. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.code import Code
from digitaloceanapi.models.error import Error
from digitaloceanapi.models.v_2_apps_rollback_validate_response import V2AppsRollbackValidateResponse
from digitaloceanapi.models.warning import Warning

v_2_apps_rollback_validate_response = V2AppsRollbackValidateResponse(
    error=Error(
        code=Code.INCOMPATIBLE_PHASE,
        components=[
            'components3'
        ],
        message='message4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    valid=False,
    warnings=[
        Warning(
            code=Code.EXCEEDED_REVISION_LIMIT,
            components=[
                'components3'
            ],
            message='message4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Warning(
            code=Code.EXCEEDED_REVISION_LIMIT,
            components=[
                'components3'
            ],
            message='message4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Warning(
            code=Code.EXCEEDED_REVISION_LIMIT,
            components=[
                'components3'
            ],
            message='message4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



