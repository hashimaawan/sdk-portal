# Result Reuse by Age Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9uMg

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseByAgeConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Enabled` | `boolean` | Required | - | boolean getEnabled() | setEnabled(boolean enabled) |
| `MaxAgeInMinutes` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 10080` | Integer getMaxAgeInMinutes() | setMaxAgeInMinutes(Integer maxAgeInMinutes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration2;
import java.io.IOException;

ResultReuseByAgeConfiguration2 resultReuseByAgeConfiguration2 = new ResultReuseByAgeConfiguration2.Builder(
    false
)
.maxAgeInMinutes(44)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



