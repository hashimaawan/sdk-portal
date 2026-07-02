# Get Calculation Execution Code Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlcXVlc3Q


# Class Name

`GetCalculationExecutionCodeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CalculationExecutionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | String getCalculationExecutionId() | setCalculationExecutionId(String calculationExecutionId) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetCalculationExecutionCodeRequest;

GetCalculationExecutionCodeRequest getCalculationExecutionCodeRequest = new GetCalculationExecutionCodeRequest.Builder(
    "CalculationExecutionId4"
)
.build();
```



