# V2 Functions Namespaces Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Namespaces` | [`[]models.Namespace`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/namespace.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2FunctionsNamespacesResponse := models.V2FunctionsNamespacesResponse{
        Namespaces:            []models.Namespace{
            models.Namespace{
                ApiHost:               models.ToPointer("api_host8"),
                CreatedAt:             models.ToPointer("created_at0"),
                Key:                   models.ToPointer("key2"),
                Label:                 models.ToPointer("label2"),
                Namespace:             models.ToPointer("namespace0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Namespace{
                ApiHost:               models.ToPointer("api_host8"),
                CreatedAt:             models.ToPointer("created_at0"),
                Key:                   models.ToPointer("key2"),
                Label:                 models.ToPointer("label2"),
                Namespace:             models.ToPointer("namespace0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



