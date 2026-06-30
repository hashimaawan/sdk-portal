# Disallows Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkRpc2FsbG93c09iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`DisallowsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InterruptingPlayback` | `*bool` | Optional | Interrupting playback. Optional field. |
| `Pausing` | `*bool` | Optional | Pausing. Optional field. |
| `Resuming` | `*bool` | Optional | Resuming. Optional field. |
| `Seeking` | `*bool` | Optional | Seeking playback location. Optional field. |
| `SkippingNext` | `*bool` | Optional | Skipping to the next context. Optional field. |
| `SkippingPrev` | `*bool` | Optional | Skipping to the previous context. Optional field. |
| `TogglingRepeatContext` | `*bool` | Optional | Toggling repeat context flag. Optional field. |
| `TogglingShuffle` | `*bool` | Optional | Toggling shuffle flag. Optional field. |
| `TogglingRepeatTrack` | `*bool` | Optional | Toggling repeat track flag. Optional field. |
| `TransferringPlayback` | `*bool` | Optional | Transfering playback between devices. Optional field. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    disallowsObject := models.DisallowsObject{
        InterruptingPlayback:  models.ToPointer(false),
        Pausing:               models.ToPointer(false),
        Resuming:              models.ToPointer(false),
        Seeking:               models.ToPointer(false),
        SkippingNext:          models.ToPointer(false),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



