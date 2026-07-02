# Start Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXF1ZXN0


# Class Name

`StartCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `CalculationConfiguration` | [`GetCalculationExecutionCodeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/get-calculation-execution-code-response.md) | Optional | - |
| `CodeBlock` | `string` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `ClientRequestToken` | `string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |


# Example

```csharp
using AmazonAthena.Standard.Models;

StartCalculationExecutionRequest startCalculationExecutionRequest = new StartCalculationExecutionRequest
{
    SessionId = "SessionId4",
    Description = "Description2",
    CalculationConfiguration = new GetCalculationExecutionCodeResponse
    {
        CodeBlock = "CodeBlock4",
    },
    CodeBlock = "CodeBlock6",
    ClientRequestToken = "ClientRequestToken8",
};
```



