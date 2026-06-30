# Http

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkh0dHA

Additional configuration for protocol http


# Class Name

`Http`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domain` | `str` | Required | Host header to send in the HTTP request. May not contain spaces, percent or backslash symbols. Can be null, in that case no host header is sent. |
| `path` | `str` | Required | HTTP path to use for health checks. May not contain literal spaces, use percent-encoding instead. |
| `response` | `str` | Optional | String that must be contained in HTTP response in order to pass the health check |
| `status_codes` | `List[str]` | Optional | List of returned HTTP status codes in order to pass the health check. Supports the wildcards `?` for exactly one character and `*` for multiple ones. The default is to pass the health check for any status code between 2?? and 3??. |
| `tls` | `bool` | Optional | Use HTTPS for health check |


# Example

```python
from hetznercloudapi.models.http import Http

http = Http(
    domain='example.com',
    path='/',
    response='{"status": "ok"}',
    status_codes=[
        '2??',
        '3??'
    ],
    tls=False
)
```



