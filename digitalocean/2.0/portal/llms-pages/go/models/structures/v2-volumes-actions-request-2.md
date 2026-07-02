# V2 Volumes Actions Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2VolumesActionsRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Region` | [`*models.Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. |
| `Type` | [`models.Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-21.md) | Required | The volume action to initiate. |
| `SizeGigabytes` | `int` | Required | The new size of the block storage volume in GiB (1024^3).<br><br>**Constraints**: `<= 16384` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2VolumesActionsRequest2 := models.V2VolumesActionsRequest2{
        Region:                models.ToPointer(models.Region2_Nyc3),
        Type:                  models.Type21_Attach,
        SizeGigabytes:         15384,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



