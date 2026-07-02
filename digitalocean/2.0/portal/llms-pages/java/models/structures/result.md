# Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdA

*This model accepts additional fields of type Object.*


# Class Name

`Result`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Metric` | `Map<String, String>` | Required | An object containing the metric labels. | Map<String, String> getMetric() | setMetric(Map<String, String> metric) |
| `Values` | [`List<List<ResultValues>>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/result-values.md) | Required | This is 2d List of a container for one-of cases. | List<List<ResultValues>> getValues() | setValues(List<List<ResultValues>> values) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Result;
import com.digitalocean.api.models.containers.ResultValues;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

Result result = new Result.Builder(
    new LinkedHashMap<String, String>() {{
        put("host_id", "19201920");
    }},
    Arrays.asList(
        Arrays.asList(
            ResultValues.fromNumber(
                1435781430
            ),
            ResultValues.fromString(
                "1"
            )
        ),
        Arrays.asList(
            ResultValues.fromNumber(
                1435781445
            ),
            ResultValues.fromString(
                "1"
            )
        )
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



