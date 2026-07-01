# HttpResponse

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGSFRUUCUyRkh0dHBSZXNwb25zZQ

Http response received.

# Parameters

| Name | Type | Description |
|  --- | --- | --- |
| status_code | `int` | The status code returned by the server. |
| reason_phrase | `str` | The reason phrase returned by the server. |
| headers | `dict` | Response headers. |
| text | `str` | Response body. |
| request | [`HttpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/http/httprequest.md) | The request that resulted in this response. |



