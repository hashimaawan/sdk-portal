# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |
| `Calculations` | [`List<CalculationSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` | List<CalculationSummary> getCalculations() | setCalculations(List<CalculationSummary> calculations) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState1Enum;
import com.amazonaws.useast1.athena.models.CalculationSummary;
import com.amazonaws.useast1.athena.models.ListCalculationExecutionsResponse;
import com.amazonaws.useast1.athena.models.Status1;
import java.util.Arrays;

ListCalculationExecutionsResponse listCalculationExecutionsResponse = new ListCalculationExecutionsResponse.Builder()
    .nextToken("NextToken8")
    .calculations(Arrays.asList(
        new CalculationSummary.Builder()
            .calculationExecutionId("CalculationExecutionId0")
            .description("Description2")
            .status(new Status1.Builder()
                .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .state(CalculationExecutionState1Enum.CANCELING)
                .stateChangeReason("StateChangeReason8")
                .build())
            .build()
    ))
    .build();
```



