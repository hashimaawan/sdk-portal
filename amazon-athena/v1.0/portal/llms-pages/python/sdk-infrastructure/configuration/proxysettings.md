# ProxySettings

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGQ29uZmlndXJhdGlvbiUyRlByb3h5U2V0dGluZ3M


Represents the proxy server configurations for API calls.

# Properties

| Name | Type | Tag | Description |
|  --- | --- | --- | --- |
| address | `str` | required | The proxy server URL. |
| port | `int` | optional | The port to connect to the proxy server. |
| username | `str` | optional | Username for proxy authentication. |
| password | `str` | optional | Password for proxy authentication. |

# Usage Example

```python
from amazonathena.amazonathena_client import AmazonathenaClient
from amazonathena.http.proxy_settings import ProxySettings

client = AmazonathenaClient(
    proxy_settings=ProxySettings(
        address='http://localhost',
        port=8888,
        username='user',
        password='pass'
     )
)
```



