# Alert

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFsZXJ0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Alert`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disabled` | `bool` | Optional | Is the alert disabled? |
| `operator` | [`Operator`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/operator.md) | Optional | **Default**: `"UNSPECIFIED_OPERATOR"` |
| `rule` | [`Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/rule.md) | Optional | **Default**: `"UNSPECIFIED_RULE"` |
| `value` | `float` | Optional | Threshold value for alert |
| `window` | [`Window`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/window.md) | Optional | **Default**: `"UNSPECIFIED_WINDOW"` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alert import Alert
from digitaloceanapi.models.operator import Operator
from digitaloceanapi.models.rule import Rule
from digitaloceanapi.models.window import Window

alert = Alert(
    disabled=False,
    operator=Operator.GREATER_THAN,
    rule=Rule.CPU_UTILIZATION,
    value=2.32,
    window=Window.FIVE_MINUTES,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



