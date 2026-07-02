# Get Calculation Execution Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`GetCalculationExecutionStatusRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CalculationExecutionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | String getCalculationExecutionId() | setCalculationExecutionId(String calculationExecutionId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetCalculationExecutionStatusRequest;
import java.io.IOException;

GetCalculationExecutionStatusRequest getCalculationExecutionStatusRequest = new GetCalculationExecutionStatusRequest.Builder(
    "CalculationExecutionId8"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



