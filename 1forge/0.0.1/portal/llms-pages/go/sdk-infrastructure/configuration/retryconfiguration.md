# RetryConfiguration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/go/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGQ29uZmlndXJhdGlvbiUyRlJldHJ5Q29uZmlndXJhdGlvbg

The following parameters are configurable for the RetryConfiguration:

# Properties

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| maxRetryAttempts | `int64` | Maximum number of retries.<br>*Default*: `0` | `WithMaxRetryAttempts` | `MaxRetryAttempts()` |
| retryOnTimeout | `bool` | Whether to retry on request timeout.<br>*Default*: `true` | `WithRetryOnTimeout` | `RetryOnTimeout()` |
| retryInterval | `timeDuration` | Interval before next retry. Used in calculation of wait time for next request in case of failure.<br>*Default*: `1` | `WithRetryInterval` | `RetryInterval()` |
| maximumRetryWaitTime | `timeDuration` | Overall wait time for the requests getting retried.<br>*Default*: `0` | `WithMaximumRetryWaitTime` | `MaximumRetryWaitTime()` |
| backoffFactor | `int64` | Used in calculation of wait time for next request in case of failure.<br>*Default*: `2` | `WithBackoffFactor` | `BackoffFactor()` |
| httpStatusCodesToRetry | `[]int64` | Http status codes to retry against.<br>*Default*: `[]int64{408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524}` | `WithHttpStatusCodesToRetry` | `HttpStatusCodesToRetry()` |
| httpMethodsToRetry | `[]string` | Http methods to retry against.<br>*Default*: `[]string{"GET", "PUT", "GET", "PUT"}` | `WithHttpMethodsToRetry` | `HttpMethodsToRetry()` |

The retryConfiguration can be initialized as follows:

```go
package main

import (
    "m1forgefinanceapis"
)

func main() {
    retryConfiguration := m1forgefinanceapis.CreateRetryConfiguration(
        m1forgefinanceapis.WithMaxRetryAttempts(0),
        m1forgefinanceapis.WithRetryOnTimeout(true),
        m1forgefinanceapis.WithRetryInterval(1),
        m1forgefinanceapis.WithMaximumRetryWaitTime(0),
        m1forgefinanceapis.WithBackoffFactor(2),
        m1forgefinanceapis.WithHttpStatusCodesToRetry([]int64{408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524}),
        m1forgefinanceapis.WithHttpMethodsToRetry([]string{"GET", "PUT", "GET", "PUT"}),
    )
}
```



