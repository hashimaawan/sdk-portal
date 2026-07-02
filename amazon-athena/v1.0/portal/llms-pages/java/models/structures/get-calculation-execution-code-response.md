# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CodeBlock` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` | String getCodeBlock() | setCodeBlock(String codeBlock) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetCalculationExecutionCodeResponse;
import java.io.IOException;

GetCalculationExecutionCodeResponse getCalculationExecutionCodeResponse = new GetCalculationExecutionCodeResponse.Builder()
    .codeBlock("CodeBlock4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



