# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CodeBlock` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` | String getCodeBlock() | setCodeBlock(String codeBlock) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CalculationConfiguration;
import java.io.IOException;

CalculationConfiguration calculationConfiguration = new CalculationConfiguration.Builder()
    .codeBlock("CodeBlock2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



