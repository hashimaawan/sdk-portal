# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | `str` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.servers_actions_attach_iso_request import ServersActionsAttachIsoRequest

servers_actions_attach_iso_request = ServersActionsAttachIsoRequest(
    iso='FreeBSD-11.0-RELEASE-amd64-dvd1',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



