# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`CalculationExecutionState4Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-4.md) | Optional | - | CalculationExecutionState4Enum getState() | setState(CalculationExecutionState4Enum state) |


# Example

```java
import com.amazonaws.useast1.athena.models.CalculationExecutionState4Enum;
import com.amazonaws.useast1.athena.models.StopCalculationExecutionResponse;

StopCalculationExecutionResponse stopCalculationExecutionResponse = new StopCalculationExecutionResponse.Builder()
    .state(CalculationExecutionState4Enum.QUEUED)
    .build();
```



