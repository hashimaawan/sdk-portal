# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ReusedPreviousResult` | `boolean` | Required | - | boolean getReusedPreviousResult() | setReusedPreviousResult(boolean reusedPreviousResult) |


# Example

```java
import com.amazonaws.useast1.athena.models.ResultReuseInformation;

ResultReuseInformation resultReuseInformation = new ResultReuseInformation.Builder(
    false
)
.build();
```



