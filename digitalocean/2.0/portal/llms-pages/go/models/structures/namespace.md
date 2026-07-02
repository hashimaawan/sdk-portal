# Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk5hbWVzcGFjZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Namespace`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApiHost` | `*string` | Optional | The namespace's API hostname. Each function in a namespace is provided an endpoint at the namespace's hostname. |
| `CreatedAt` | `*string` | Optional | UTC time string. |
| `Key` | `*string` | Optional | A random alpha numeric string. This key is used in conjunction with the namespace's UUID to authenticate<br>a user to use the namespace via `doctl`, DigitalOcean's official CLI. |
| `Label` | `*string` | Optional | The namespace's unique name. |
| `Namespace` | `*string` | Optional | A unique string format of UUID with a prefix fn-. |
| `Region` | `*string` | Optional | The namespace's datacenter region. |
| `UpdatedAt` | `*string` | Optional | UTC time string. |
| `Uuid` | `*string` | Optional | The namespace's Universally Unique Identifier. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    namespace := models.Namespace{
        ApiHost:               models.ToPointer("https://api_host.io"),
        CreatedAt:             models.ToPointer("2022-09-14T04:16:45Z"),
        Key:                   models.ToPointer("d1zcd455h01mqjfs4s2eaewyejehi5f2uj4etqq3h7cera8iwkub6xg5of1wdde2"),
        Label:                 models.ToPointer("my namespace"),
        Namespace:             models.ToPointer("fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"),
        Region:                models.ToPointer("nyc1"),
        UpdatedAt:             models.ToPointer("2022-09-14T04:16:45Z"),
        Uuid:                  models.ToPointer("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



