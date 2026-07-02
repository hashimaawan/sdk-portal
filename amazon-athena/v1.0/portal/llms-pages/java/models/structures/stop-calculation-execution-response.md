# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`CalculationExecutionState4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-4.md) | Optional | - | CalculationExecutionState4 getState() | setState(CalculationExecutionState4 state) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState4;
import com.amazonaws.useast1.athena.models.StopCalculationExecutionResponse;
import java.io.IOException;

StopCalculationExecutionResponse stopCalculationExecutionResponse = new StopCalculationExecutionResponse.Builder()
    .state(CalculationExecutionState4.QUEUED)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



