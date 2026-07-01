# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |
| `password` | `str` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) |
| `wss_url` | `str` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.servers_actions_request_console_response import ServersActionsRequestConsoleResponse
from hetznercloudapi.models.status import Status

servers_actions_request_console_response = ServersActionsRequestConsoleResponse(
    action=Action(
        command='start_server',
        error=Error(
            code='action_failed',
            message='Action failed',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        finished='2016-01-30T23:55:00+00:00',
        id=42,
        progress=100,
        resources=[
            Resource(
                id=42,
                mtype='server',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        started='2016-01-30T23:55:00+00:00',
        status=Status.RUNNING,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    password='9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x',
    wss_url='wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



