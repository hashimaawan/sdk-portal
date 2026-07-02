# Stop Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlcXVlc3Q


# Class Name

`StopCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CalculationExecutionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | String getCalculationExecutionId() | setCalculationExecutionId(String calculationExecutionId) |


# Example

```java
import com.amazonaws.useast1.athena.models.StopCalculationExecutionRequest;

StopCalculationExecutionRequest stopCalculationExecutionRequest = new StopCalculationExecutionRequest.Builder(
    "CalculationExecutionId2"
)
.build();
```



