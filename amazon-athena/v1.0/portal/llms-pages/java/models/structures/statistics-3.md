# Statistics 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mz

*This model accepts additional fields of type Object.*


# Class Name

`Statistics3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DpuExecutionInMillis` | `Integer` | Optional | - | Integer getDpuExecutionInMillis() | setDpuExecutionInMillis(Integer dpuExecutionInMillis) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Statistics3;
import java.io.IOException;

Statistics3 statistics3 = new Statistics3.Builder()
    .dpuExecutionInMillis(130)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



