# Http

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkh0dHA

Additional configuration for protocol http


# Class Name

`Http`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Domain` | `*string` | Required | Host header to send in the HTTP request. May not contain spaces, percent or backslash symbols. Can be null, in that case no host header is sent. |
| `Path` | `string` | Required | HTTP path to use for health checks. May not contain literal spaces, use percent-encoding instead. |
| `Response` | `*string` | Optional | String that must be contained in HTTP response in order to pass the health check |
| `StatusCodes` | `[]string` | Optional | List of returned HTTP status codes in order to pass the health check. Supports the wildcards `?` for exactly one character and `*` for multiple ones. The default is to pass the health check for any status code between 2?? and 3??. |
| `Tls` | `*bool` | Optional | Use HTTPS for health check |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    http := models.Http{
        Domain:      models.ToPointer("example.com"),
        Path:        "/",
        Response:    models.ToPointer("{\"status\": \"ok\"}"),
        StatusCodes: []string{
            "2??",
            "3??",
        },
        Tls:         models.ToPointer(false),
    }

}
```



