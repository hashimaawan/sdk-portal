# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Enabled` | `boolean` | Required | - | boolean getEnabled() | setEnabled(boolean enabled) |
| `MaxAgeInMinutes` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 10080` | Integer getMaxAgeInMinutes() | setMaxAgeInMinutes(Integer maxAgeInMinutes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration;
import java.io.IOException;

ResultReuseByAgeConfiguration resultReuseByAgeConfiguration = new ResultReuseByAgeConfiguration.Builder(
    false
)
.maxAgeInMinutes(134)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



