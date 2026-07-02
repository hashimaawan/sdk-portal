# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type interface{}.*


# Class Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`*models.SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/session-state-1.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    terminateSessionResponse := models.TerminateSessionResponse{
        State:                 models.ToPointer(models.SessionState1_Creating),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



