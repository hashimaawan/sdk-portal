# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListApplicationDpuSizesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApplicationDpuSizes` | [`List<ApplicationDpuSizes>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/application-dpu-sizes.md) | Optional | - | List<ApplicationDpuSizes> getApplicationDpuSizes() | setApplicationDpuSizes(List<ApplicationDpuSizes> applicationDpuSizes) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ApplicationDpuSizes;
import com.amazonaws.useast1.athena.models.ListApplicationDpuSizesOutput;
import java.io.IOException;
import java.util.Arrays;

ListApplicationDpuSizesOutput listApplicationDpuSizesOutput = new ListApplicationDpuSizesOutput.Builder()
    .applicationDpuSizes(Arrays.asList(
        new ApplicationDpuSizes.Builder()
            .applicationRuntimeId("ApplicationRuntimeId0")
            .supportedDpuSizes(Arrays.asList(
                113,
                114
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ApplicationDpuSizes.Builder()
            .applicationRuntimeId("ApplicationRuntimeId0")
            .supportedDpuSizes(Arrays.asList(
                113,
                114
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .nextToken("NextToken0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



