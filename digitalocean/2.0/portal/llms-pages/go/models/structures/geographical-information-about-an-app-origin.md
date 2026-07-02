# Geographical Information about an App Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkdlb2dyYXBoaWNhbCUyNTIwaW5mb3JtYXRpb24lMjUyMGFib3V0JTI1MjBhbiUyNTIwYXBwJTI1MjBvcmlnaW4

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`GeographicalInformationAboutAnAppOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Continent` | `*string` | Optional, Read-only | - |
| `DataCenters` | `[]string` | Optional, Read-only | - |
| `Default` | `*bool` | Optional, Read-only | Whether or not the region is presented as the default. |
| `Disabled` | `*bool` | Optional, Read-only | - |
| `Flag` | `*string` | Optional, Read-only | - |
| `Label` | `*string` | Optional, Read-only | - |
| `Reason` | `*string` | Optional, Read-only | - |
| `Slug` | `*string` | Optional, Read-only | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    geographicalInformationAboutAnAppOrigin := models.GeographicalInformationAboutAnAppOrigin{
        Continent:             models.ToPointer("europe"),
        DataCenters:           []string{
            "ams",
        },
        Default:               models.ToPointer(true),
        Disabled:              models.ToPointer(true),
        Flag:                  models.ToPointer("ams"),
        Label:                 models.ToPointer("ams"),
        Reason:                models.ToPointer("to crowded"),
        Slug:                  models.ToPointer("basic"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



