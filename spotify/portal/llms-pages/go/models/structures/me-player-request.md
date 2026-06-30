# Me Player Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRk1lJTI1MjBQbGF5ZXIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`MePlayerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeviceIds` | `[]string` | Required | A JSON array containing the ID of the device on which playback should be started/transferred.<br/>For example:`{device_ids:["74ASZWbe4lXaubB36ztrGX"]}`<br/>_**Note**: Although an array is accepted, only a single device_id is currently supported. Supplying more than one will return `400 Bad Request`_ |
| `Play` | `*bool` | Optional | **true**: ensure playback happens on new device.<br/>**false** or not provided: keep the current playback state. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    mePlayerRequest := models.MePlayerRequest{
        DeviceIds:             []string{
            "74ASZWbe4lXaubB36ztrGX",
        },
        Play:                  models.ToPointer(false),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



