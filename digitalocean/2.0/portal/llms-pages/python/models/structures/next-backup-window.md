# Next Backup Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk5leHRCYWNrdXBXaW5kb3c

The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`NextBackupWindow`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `end` | `datetime` | Optional | A time value given in ISO8601 combined date and time format specifying the end of the Droplet's backup window. |
| `start` | `datetime` | Optional | A time value given in ISO8601 combined date and time format specifying the start of the Droplet's backup window. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.next_backup_window import NextBackupWindow

next_backup_window = NextBackupWindow(
    end=dateutil.parser.parse('2019-12-04T23:00:00Z'),
    start=dateutil.parser.parse('2019-12-04T00:00:00Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



