# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CodeBlock` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` | String getCodeBlock() | setCodeBlock(String codeBlock) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetCalculationExecutionCodeResponse;

GetCalculationExecutionCodeResponse getCalculationExecutionCodeResponse = new GetCalculationExecutionCodeResponse.Builder()
    .codeBlock("CodeBlock4")
    .build();
```



