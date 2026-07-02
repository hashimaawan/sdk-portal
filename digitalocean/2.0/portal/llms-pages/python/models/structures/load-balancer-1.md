# Load Balancer 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcjE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`LoadBalancer1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/algorithm.md) | Optional | This field has been deprecated. You can no longer specify an algorithm for load balancers.<br><br>**Default**: `"round_robin"` |
| `created_at` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the load balancer was created. |
| `disable_lets_encrypt_dns_records` | `bool` | Optional | A boolean value indicating whether to disable automatic DNS record creation for Let's Encrypt certificates that are added to the load balancer.<br><br>**Default**: `False` |
| `enable_backend_keepalive` | `bool` | Optional | A boolean value indicating whether HTTP keepalive connections are maintained to target Droplets.<br><br>**Default**: `False` |
| `enable_proxy_protocol` | `bool` | Optional | A boolean value indicating whether PROXY Protocol is in use.<br><br>**Default**: `False` |
| `firewall` | [`Firewall1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/firewall-1.md) | Optional | An object specifying allow and deny rules to control traffic to the load balancer. |
| `forwarding_rules` | [`List[ForwardingRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/forwarding-rule.md) | Required | An array of objects specifying the forwarding rules for a load balancer.<br><br>**Constraints**: *Minimum Items*: `1` |
| `health_check` | [`HealthCheck1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/health-check-1.md) | Optional | An object specifying health check settings for the load balancer. |
| `http_idle_timeout_seconds` | `int` | Optional | An integer value which configures the idle timeout for HTTP requests to the target droplets.<br><br>**Default**: `60`<br><br>**Constraints**: `>= 30`, `<= 600` |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference a load balancer. |
| `ip` | `str` | Optional, Read-only | An attribute containing the public-facing IP address of the load balancer.<br><br>**Constraints**: *Pattern*: `^$\|^((25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)\.){3}(25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)$` |
| `name` | `str` | Optional | A human-readable name for a load balancer instance. |
| `project_id` | `str` | Optional | The ID of the project that the load balancer is associated with. If no ID is provided at creation, the load balancer associates with the user's default project. If an invalid project ID is provided, the load balancer will not be created. |
| `redirect_http_to_https` | `bool` | Optional | A boolean value indicating whether HTTP requests to the load balancer on port 80 will be redirected to HTTPS on port 443.<br><br>**Default**: `False` |
| `size` | [`Size2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/size-2.md) | Optional | This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.<br><br>* `lb-small` = 1 node<br>* `lb-medium` = 3 nodes<br>* `lb-large` = 6 nodes<br><br>You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.<br><br>**Default**: `"lb-small"` |
| `size_unit` | `int` | Optional | How many nodes the load balancer contains. Each additional node increases the load balancer's ability to manage more connections. Load balancers can be scaled up or down, and you can change the number of nodes after creation up to once per hour. This field is currently not available in the AMS2, NYC2, or SFO1 regions. Use the `size` field to scale load balancers that reside in these regions.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `status` | [`Status12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-12.md) | Optional, Read-only | A status string indicating the current state of the load balancer. This can be `new`, `active`, or `errored`. |
| `sticky_sessions` | [`StickySessions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/sticky-sessions.md) | Optional | An object specifying sticky sessions settings for the load balancer. |
| `vpc_uuid` | `uuid\|str` | Optional | A string specifying the UUID of the VPC to which the load balancer is assigned. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/region.md) | Optional | - |
| `droplet_ids` | `List[int]` | Optional | An array containing the IDs of the Droplets assigned to the load balancer. |
| `tag` | `str` | Optional | The name of a Droplet tag corresponding to Droplets assigned to the load balancer. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.algorithm import Algorithm
from digitaloceanapi.models.entry_protocol import EntryProtocol
from digitaloceanapi.models.forwarding_rule import ForwardingRule
from digitaloceanapi.models.load_balancer_1 import LoadBalancer1
from digitaloceanapi.models.size_2 import Size2
from digitaloceanapi.models.status_12 import Status12
from digitaloceanapi.models.target_protocol import TargetProtocol

load_balancer_1 = LoadBalancer1(
    forwarding_rules=[
        ForwardingRule(
            entry_port=443,
            entry_protocol=EntryProtocol.HTTPS,
            target_port=80,
            target_protocol=TargetProtocol.HTTP,
            certificate_id='892071a0-bb95-49bc-8021-3afd67a210bf',
            tls_passthrough=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    algorithm=Algorithm.ROUND_ROBIN,
    created_at=dateutil.parser.parse('2017-02-01T22:22:58Z'),
    disable_lets_encrypt_dns_records=True,
    enable_backend_keepalive=True,
    enable_proxy_protocol=True,
    http_idle_timeout_seconds=90,
    id='4de7ac8b-495b-4884-9a69-1050c6793cd6',
    ip='104.131.186.241',
    name='example-lb-01',
    project_id='4de7ac8b-495b-4884-9a69-1050c6793cd6',
    redirect_http_to_https=True,
    size=Size2.LBSMALL,
    size_unit=3,
    status=Status12.NEW,
    vpc_uuid='c33931f2-a26a-4e61-b85c-4e95a2ec431b',
    droplet_ids=[
        3164444,
        3164445
    ],
    tag='prod:web',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



