# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CalculationExecutionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | String getCalculationExecutionId() | setCalculationExecutionId(String calculationExecutionId) |
| `State` | [`CalculationExecutionState4Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-4.md) | Optional | - | CalculationExecutionState4Enum getState() | setState(CalculationExecutionState4Enum state) |


# Example

```java
import com.amazonaws.useast1.athena.models.CalculationExecutionState4Enum;
import com.amazonaws.useast1.athena.models.StartCalculationExecutionResponse;

StartCalculationExecutionResponse startCalculationExecutionResponse = new StartCalculationExecutionResponse.Builder()
    .calculationExecutionId("CalculationExecutionId0")
    .state(CalculationExecutionState4Enum.CANCELING)
    .build();
```



