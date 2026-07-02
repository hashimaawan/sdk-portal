# Start Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXF1ZXN0


# Class Name

`StartCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `CalculationConfiguration` | [`*models.GetCalculationExecutionCodeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/get-calculation-execution-code-response.md) | Optional | - |
| `CodeBlock` | `*string` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `ClientRequestToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    startCalculationExecutionRequest := models.StartCalculationExecutionRequest{
        SessionId:                "SessionId4",
        Description:              models.ToPointer("Description2"),
        CalculationConfiguration: models.ToPointer(models.GetCalculationExecutionCodeResponse{
            CodeBlock:            models.ToPointer("CodeBlock4"),
        }),
        CodeBlock:                models.ToPointer("CodeBlock6"),
        ClientRequestToken:       models.ToPointer("ClientRequestToken8"),
    }

}
```



