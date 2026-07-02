# V2 Droplets Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing information about a resource to be scheduled for deletion.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | `[]string` | Optional | An array of unique identifiers for the floating IPs to be scheduled for deletion. |
| `ReservedIps` | `[]string` | Optional | An array of unique identifiers for the reserved IPs to be scheduled for deletion. |
| `Snapshots` | `[]string` | Optional | An array of unique identifiers for the snapshots to be scheduled for deletion. |
| `VolumeSnapshots` | `[]string` | Optional | An array of unique identifiers for the volume snapshots to be scheduled for deletion. |
| `Volumes` | `[]string` | Optional | An array of unique identifiers for the volumes to be scheduled for deletion. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DropletsDestroyWithAssociatedResourcesSelectiveRequest := models.V2DropletsDestroyWithAssociatedResourcesSelectiveRequest{
        FloatingIps:           []string{
            "6186916",
        },
        ReservedIps:           []string{
            "6186916",
        },
        Snapshots:             []string{
            "61486916",
        },
        VolumeSnapshots:       []string{
            "edb0478d-7436-11ea-86e6-0a58ac144b91",
        },
        Volumes:               []string{
            "ba49449a-7435-11ea-b89e-0a58ac14480f",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



