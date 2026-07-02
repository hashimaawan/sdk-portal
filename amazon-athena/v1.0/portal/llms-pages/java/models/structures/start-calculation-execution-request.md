# Start Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXF1ZXN0


# Class Name

`StartCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `CalculationConfiguration` | [`GetCalculationExecutionCodeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/get-calculation-execution-code-response.md) | Optional | - | GetCalculationExecutionCodeResponse getCalculationConfiguration() | setCalculationConfiguration(GetCalculationExecutionCodeResponse calculationConfiguration) |
| `CodeBlock` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` | String getCodeBlock() | setCodeBlock(String codeBlock) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetCalculationExecutionCodeResponse;
import com.amazonaws.useast1.athena.models.StartCalculationExecutionRequest;

StartCalculationExecutionRequest startCalculationExecutionRequest = new StartCalculationExecutionRequest.Builder(
    "SessionId4"
)
.description("Description2")
.calculationConfiguration(new GetCalculationExecutionCodeResponse.Builder()
        .codeBlock("CodeBlock4")
        .build())
.codeBlock("CodeBlock6")
.clientRequestToken("ClientRequestToken8")
.build();
```



