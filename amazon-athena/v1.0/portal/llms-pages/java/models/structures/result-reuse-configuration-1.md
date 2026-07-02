# Result Reuse Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbjE

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResultReuseByAgeConfiguration` | [`ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - | ResultReuseByAgeConfiguration2 getResultReuseByAgeConfiguration() | setResultReuseByAgeConfiguration(ResultReuseByAgeConfiguration2 resultReuseByAgeConfiguration) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration2;
import com.amazonaws.useast1.athena.models.ResultReuseConfiguration1;
import java.io.IOException;

ResultReuseConfiguration1 resultReuseConfiguration1 = new ResultReuseConfiguration1.Builder()
    .resultReuseByAgeConfiguration(new ResultReuseByAgeConfiguration2.Builder(
        false
    )
    .maxAgeInMinutes(26)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



