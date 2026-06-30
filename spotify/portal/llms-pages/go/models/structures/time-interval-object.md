# Time Interval Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlRpbWVJbnRlcnZhbE9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`TimeIntervalObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Start` | `*float64` | Optional | The starting point (in seconds) of the time interval. |
| `Duration` | `*float64` | Optional | The duration (in seconds) of the time interval. |
| `Confidence` | `*float64` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the interval.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    timeIntervalObject := models.TimeIntervalObject{
        Start:                 models.ToPointer(float64(0.49567)),
        Duration:              models.ToPointer(float64(2.18749)),
        Confidence:            models.ToPointer(float64(0.925)),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



