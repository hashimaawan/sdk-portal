# Maintenance Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlV2luZG93

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`MaintenanceWindow`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `day` | `str` | Required | The day of the week on which to apply maintenance updates. |
| `description` | `List[str]` | Optional, Read-only | A list of strings, each containing information about a pending maintenance update. |
| `hour` | `str` | Required | The hour in UTC at which maintenance updates will be applied in 24 hour format. |
| `pending` | `bool` | Optional, Read-only | A boolean value indicating whether any maintenance is scheduled to be performed in the next window. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.maintenance_window import MaintenanceWindow

maintenance_window = MaintenanceWindow(
    day='tuesday',
    hour='14:00',
    description=[
        'Update TimescaleDB to version 1.2.1',
        'Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases'
    ],
    pending=True,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



