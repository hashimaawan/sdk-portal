# Data

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGE

*This model accepts additional fields of type Object.*


# Class Name

`Data`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Result` | [`List<Result>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/result.md) | Required | Result of query. | List<Result> getResult() | setResult(List<Result> result) |
| `ResultType` | `String` | Required, Constant | **Value**: `"matrix"` | String getResultType() | setResultType(String resultType) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Data;
import com.digitalocean.api.models.Result;
import com.digitalocean.api.models.containers.ResultValues;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

Data data = new Data.Builder(
    Arrays.asList(
        new Result.Builder(
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
        .build()
    ),
    "matrix"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



