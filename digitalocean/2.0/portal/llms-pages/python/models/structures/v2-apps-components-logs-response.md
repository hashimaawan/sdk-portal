# V2 Apps Components Logs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBDb21wb25lbnRzJTI1MjBMb2dzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsComponentsLogsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `historic_urls` | `List[str]` | Optional | - |
| `live_url` | `str` | Optional | A URL of the real-time live logs. This URL may use either the `https://` or `wss://` protocols and will keep pushing live logs as they become available. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_apps_components_logs_response import V2AppsComponentsLogsResponse

v_2_apps_components_logs_response = V2AppsComponentsLogsResponse(
    historic_urls=[
        'historic_urls9',
        'historic_urls8',
        'historic_urls7'
    ],
    live_url='ws://logs/build',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



