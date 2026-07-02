# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/status-1.md) | Optional | - | Status1 getStatus() | setStatus(Status1 status) |
| `Statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/statistics-1.md) | Optional | - | Statistics1 getStatistics() | setStatistics(Statistics1 statistics) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState1Enum;
import com.amazonaws.useast1.athena.models.GetCalculationExecutionStatusResponse;
import com.amazonaws.useast1.athena.models.Statistics1;
import com.amazonaws.useast1.athena.models.Status1;

GetCalculationExecutionStatusResponse getCalculationExecutionStatusResponse = new GetCalculationExecutionStatusResponse.Builder()
    .status(new Status1.Builder()
        .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .state(CalculationExecutionState1Enum.CANCELING)
        .stateChangeReason("StateChangeReason8")
        .build())
    .statistics(new Statistics1.Builder()
        .dpuExecutionInMillis(164)
        .progress("Progress6")
        .build())
    .build();
```



