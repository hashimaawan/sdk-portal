# Cors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkNvcnM

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Cors`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AllowCredentials` | `*bool` | Optional | Whether browsers should expose the response to the client-side JavaScript code when the request’s credentials mode is include. This configures the `Access-Control-Allow-Credentials` header. |
| `AllowHeaders` | `[]string` | Optional | The set of allowed HTTP request headers. This configures the `Access-Control-Allow-Headers` header. |
| `AllowMethods` | `[]string` | Optional | The set of allowed HTTP methods. This configures the `Access-Control-Allow-Methods` header. |
| `AllowOrigins` | [`[]models.AllowOrigin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/allow-origin.md) | Optional | The set of allowed CORS origins. |
| `ExposeHeaders` | `[]string` | Optional | The set of HTTP response headers that browsers are allowed to access. This configures the `Access-Control-Expose-Headers` header. |
| `MaxAge` | `*string` | Optional | An optional duration specifying how long browsers can cache the results of a preflight request. This configures the `Access-Control-Max-Age` header. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    cors := models.Cors{
        AllowCredentials:      models.ToPointer(false),
        AllowHeaders:          []string{
            "Content-Type",
            "X-Custom-Header",
        },
        AllowMethods:          []string{
            "GET",
            "OPTIONS",
            "POST",
            "PUT",
            "PATCH",
            "DELETE",
        },
        AllowOrigins:          []models.AllowOrigin{
            models.AllowOrigin{
                Exact:                 models.ToPointer("https://www.example.com"),
                Prefix:                models.ToPointer("prefix6"),
                Regex:                 models.ToPointer("regex4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.AllowOrigin{
                Exact:                 models.ToPointer("exact8"),
                Prefix:                models.ToPointer("prefix6"),
                Regex:                 models.ToPointer("^.*example.com"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        ExposeHeaders:         []string{
            "Content-Encoding",
            "X-Custom-Header",
        },
        MaxAge:                models.ToPointer("5h30m"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



