# A Criterion for Routing HTTP Traffic to a Component

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkElMjUyMGNyaXRlcmlvbiUyNTIwZm9yJTI1MjByb3V0aW5nJTI1MjBIVFRQJTI1MjB0cmFmZmljJTI1MjB0byUyNTIwYSUyNTIwY29tcG9uZW50Lg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ACriterionForRoutingHttpTrafficToAComponent`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Path` | `*string` | Optional | An HTTP path prefix. Paths must start with / and must be unique across all components within an app. |
| `PreservePathPrefix` | `*bool` | Optional | An optional flag to preserve the path that is forwarded to the backend service. By default, the HTTP request path will be trimmed from the left when forwarded to the component. For example, a component with `path=/api` will have requests to `/api/list` trimmed to `/list`. If this value is `true`, the path will remain `/api/list`. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    aCriterionForRoutingHttpTrafficToAComponent := models.ACriterionForRoutingHttpTrafficToAComponent{
        Path:                  models.ToPointer("/api"),
        PreservePathPrefix:    models.ToPointer(true),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



