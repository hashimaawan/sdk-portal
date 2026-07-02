# Pgbouncer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlBnYm91bmNlcg

PGBouncer connection pooling settings

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Pgbouncer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autodb_idle_timeout` | `int` | Optional | If the automatically-created database pools have been unused this many seconds, they are freed. If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `autodb_max_db_connections` | `int` | Optional | Only allows a maximum this many server connections per database (regardless of user). If 0, allows unlimited connections.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `autodb_pool_mode` | [`AutodbPoolMode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/autodb-pool-mode.md) | Optional | PGBouncer pool mode |
| `autodb_pool_size` | `int` | Optional | If non-zero, automatically creates a pool of that size per user when a pool doesn't exist.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `ignore_startup_parameters` | [`List[IgnoreStartupParameter]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/ignore-startup-parameter.md) | Optional | List of parameters to ignore when given in startup packet.<br><br>**Constraints**: *Maximum Items*: `32` |
| `min_pool_size` | `int` | Optional | If current server connections are below this number, adds more. Improves behavior when usual load comes suddenly back after period of total inactivity. The value is effectively capped at the pool size.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `server_idle_timeout` | `int` | Optional | Drops server connections if they have been idle more than this many seconds.  If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `server_lifetime` | `int` | Optional | The pooler closes any unused server connection that has been connected longer than this amount of seconds.<br><br>**Constraints**: `>= 60`, `<= 86400` |
| `server_reset_query_always` | `bool` | Optional | Run server_reset_query (DISCARD ALL) in all pooling modes. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.autodb_pool_mode import AutodbPoolMode
from digitaloceanapi.models.ignore_startup_parameter import IgnoreStartupParameter
from digitaloceanapi.models.pgbouncer import Pgbouncer

pgbouncer = Pgbouncer(
    autodb_idle_timeout=3600,
    autodb_max_db_connections=1,
    autodb_pool_mode=AutodbPoolMode.SESSION,
    autodb_pool_size=1,
    ignore_startup_parameters=[
        IgnoreStartupParameter.EXTRA_FLOAT_DIGITS,
        IgnoreStartupParameter.SEARCH_PATH
    ],
    min_pool_size=1,
    server_idle_timeout=600,
    server_lifetime=3600,
    server_reset_query_always=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



