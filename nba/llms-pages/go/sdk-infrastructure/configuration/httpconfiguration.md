# HttpConfiguration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/go/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGQ29uZmlndXJhdGlvbiUyRkh0dHBDb25maWd1cmF0aW9u

The following parameters are configurable for the HttpConfiguration:

# Properties

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| timeout | `float64` | Timeout in seconds.<br>*Default*: `0` | `WithTimeout` | `Timeout()` |
| transport | `httpRoundTripper` | Establishes network connection and caches them for reuse.<br>*Default*: `http.DefaultTransport` | `WithTransport` | `Transport()` |
| retryConfiguration | [`nbastatsapiRetryConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/go/sdk-infrastructure/configuration/retryconfiguration.md) | Configurations to retry requests.<br>*Default*: `nbastatsapi.DefaultRetryConfiguration()` | `WithRetryConfiguration` | `RetryConfiguration()` |

The httpConfiguration can be initialized as follows:

```go
package main

import (
    "nbastatsapi"
    "net/http"
)

func main() {
    httpConfiguration := nbastatsapi.CreateHttpConfiguration(
        nbastatsapi.WithTimeout(0),
        nbastatsapi.WithTransport(http.DefaultTransport),
        nbastatsapi.WithRetryConfiguration(nbastatsapi.DefaultRetryConfiguration()),
    )
}
```



