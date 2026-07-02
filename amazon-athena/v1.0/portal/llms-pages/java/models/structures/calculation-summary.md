# Calculation Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3VtbWFyeQ

Summary information for a notebook calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CalculationExecutionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | String getCalculationExecutionId() | setCalculationExecutionId(String calculationExecutionId) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/status-1.md) | Optional | - | Status1 getStatus() | setStatus(Status1 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState1;
import com.amazonaws.useast1.athena.models.CalculationSummary;
import com.amazonaws.useast1.athena.models.Status1;
import java.io.IOException;

CalculationSummary calculationSummary = new CalculationSummary.Builder()
    .calculationExecutionId("CalculationExecutionId4")
    .description("Description6")
    .status(new Status1.Builder()
        .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .state(CalculationExecutionState1.CANCELING)
        .stateChangeReason("StateChangeReason8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



