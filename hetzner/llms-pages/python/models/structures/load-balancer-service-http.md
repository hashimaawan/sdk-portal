# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https


# Class Name

`LoadBalancerServiceHTTP`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificates` | `List[int]` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" |
| `cookie_lifetime` | `int` | Optional | Lifetime of the cookie used for sticky sessions |
| `cookie_name` | `str` | Optional | Name of the cookie used for sticky sessions |
| `redirect_http` | `bool` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` |
| `sticky_sessions` | `bool` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` |


# Example

```python
from hetznercloudapi.models.load_balancer_service_http import LoadBalancerServiceHTTP

load_balancer_service_http = LoadBalancerServiceHTTP(
    certificates=[
        897
    ],
    cookie_lifetime=300,
    cookie_name='HCLBSTICKY',
    redirect_http=True,
    sticky_sessions=True
)
```



