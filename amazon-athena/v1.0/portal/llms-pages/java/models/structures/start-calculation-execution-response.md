# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CalculationExecutionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | String getCalculationExecutionId() | setCalculationExecutionId(String calculationExecutionId) |
| `State` | [`CalculationExecutionState4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-4.md) | Optional | - | CalculationExecutionState4 getState() | setState(CalculationExecutionState4 state) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState4;
import com.amazonaws.useast1.athena.models.StartCalculationExecutionResponse;
import java.io.IOException;

StartCalculationExecutionResponse startCalculationExecutionResponse = new StartCalculationExecutionResponse.Builder()
    .calculationExecutionId("CalculationExecutionId0")
    .state(CalculationExecutionState4.CANCELING)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



