# HttpConfiguration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGQ29uZmlndXJhdGlvbiUyRkh0dHBDb25maWd1cmF0aW9u

The following parameters are configurable for the HttpConfiguration:

# Properties

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| timeout | `float64` | Timeout in seconds.<br>*Default*: `30` | `WithTimeout` | `Timeout()` |
| transport | `httpRoundTripper` | Establishes network connection and caches them for reuse.<br>*Default*: `http.DefaultTransport` | `WithTransport` | `Transport()` |
| retryConfiguration | [`giphyApiRetryConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/sdk-infrastructure/configuration/retryconfiguration.md) | Configurations to retry requests.<br>*Default*: `giphyApi.DefaultRetryConfiguration()` | `WithRetryConfiguration` | `RetryConfiguration()` |

The httpConfiguration can be initialized as follows:

```go
package main

import (
    "giphyApi"
    "net/http"
)

func main() {
    httpConfiguration := giphyApi.CreateHttpConfiguration(
        giphyApi.WithTimeout(30),
        giphyApi.WithTransport(http.DefaultTransport),
        giphyApi.WithRetryConfiguration(giphyApi.DefaultRetryConfiguration()),
    )
}
```



