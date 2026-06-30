# HttpConfiguration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGQ29uZmlndXJhdGlvbiUyRkh0dHBDb25maWd1cmF0aW9u

The following parameters are configurable for the HttpConfiguration:

# Properties

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| timeout | `float64` | Timeout in seconds.<br>*Default*: `30` | `WithTimeout` | `Timeout()` |
| transport | `httpRoundTripper` | Establishes network connection and caches them for reuse.<br>*Default*: `http.DefaultTransport` | `WithTransport` | `Transport()` |
| retryConfiguration | [`m1PasswordConnectRetryConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/configuration/retryconfiguration.md) | Configurations to retry requests.<br>*Default*: `m1PasswordConnect.DefaultRetryConfiguration()` | `WithRetryConfiguration` | `RetryConfiguration()` |

The httpConfiguration can be initialized as follows:

```go
package main

import (
    "m1PasswordConnect"
    "net/http"
)

func main() {
    httpConfiguration := m1PasswordConnect.CreateHttpConfiguration(
        m1PasswordConnect.WithTimeout(30),
        m1PasswordConnect.WithTransport(http.DefaultTransport),
        m1PasswordConnect.WithRetryConfiguration(m1PasswordConnect.DefaultRetryConfiguration()),
    )
}
```



