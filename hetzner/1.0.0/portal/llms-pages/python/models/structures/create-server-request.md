# Create Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`CreateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `bool` | Optional | Auto-mount Volumes after attach |
| `datacenter` | `str` | Optional | ID or name of Datacenter to create Server in (must not be used together with location) |
| `firewalls` | [`List[Firewall4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/firewall-4.md) | Optional | Firewalls which should be applied on the Server's public network interface at creation time |
| `image` | `str` | Required | ID or name of the Image the Server is created from |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `location` | `str` | Optional | ID or name of Location to create Server in (must not be used together with datacenter) |
| `name` | `str` | Required | Name of the Server to create (must be unique per Project and a valid hostname as per RFC 1123) |
| `networks` | `List[int]` | Optional | Network IDs which should be attached to the Server private network interface at the creation time |
| `placement_group` | `int` | Optional | ID of the Placement Group the server should be in |
| `public_net` | [`PublicNet5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/public-net-5.md) | Optional | Public Network options |
| `server_type` | `str` | Required | ID or name of the Server type this Server should be created with |
| `ssh_keys` | `List[str]` | Optional | SSH key IDs (`integer`) or names (`string`) which should be injected into the Server at creation time |
| `start_after_create` | `bool` | Optional | Start Server right after creation. Defaults to true. |
| `user_data` | `str` | Optional | Cloud-Init user data to use during Server creation. This field is limited to 32KiB. |
| `volumes` | `List[int]` | Optional | Volume IDs which should be attached to the Server at the creation time. Volumes must be in the same Location. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_server_request import CreateServerRequest
from hetznercloudapi.models.firewall_4 import Firewall4

create_server_request = CreateServerRequest(
    image='ubuntu-20.04',
    name='my-server',
    server_type='cx11',
    automount=False,
    datacenter='nbg1-dc3',
    firewalls=[
        Firewall4(
            firewall=38,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    location='nbg1',
    networks=[
        456
    ],
    placement_group=1,
    ssh_keys=[
        'my-ssh-key'
    ],
    start_after_create=True,
    user_data='#cloud-config\nruncmd:\n- [touch, /root/cloud-init-worked]\n',
    volumes=[
        123
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



