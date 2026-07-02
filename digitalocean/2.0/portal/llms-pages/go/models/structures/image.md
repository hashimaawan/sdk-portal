# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Registry` | `*string` | Optional | The registry name. Must be left empty for the `DOCR` registry type. |
| `RegistryType` | [`*models.RegistryType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/registry-type.md) | Optional | - DOCKER_HUB: The DockerHub container registry type.<br>- DOCR: The DigitalOcean container registry type. |
| `Repository` | `*string` | Optional | The repository name. |
| `Tag` | `*string` | Optional | The repository tag. Defaults to `latest` if not provided.<br><br>**Default**: `"latest"` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    image := models.Image{
        Registry:              models.ToPointer("registry.hub.docker.com"),
        RegistryType:          models.ToPointer(models.RegistryType_Docr),
        Repository:            models.ToPointer("origin/master"),
        Tag:                   models.ToPointer("latest"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



