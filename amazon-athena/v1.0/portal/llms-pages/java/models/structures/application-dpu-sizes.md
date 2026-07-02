# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.

*This model accepts additional fields of type Object.*


# Class Name

`ApplicationDpuSizes`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApplicationRuntimeId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getApplicationRuntimeId() | setApplicationRuntimeId(String applicationRuntimeId) |
| `SupportedDpuSizes` | `List<Integer>` | Optional | - | List<Integer> getSupportedDpuSizes() | setSupportedDpuSizes(List<Integer> supportedDpuSizes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ApplicationDpuSizes;
import java.io.IOException;
import java.util.Arrays;

ApplicationDpuSizes applicationDpuSizes = new ApplicationDpuSizes.Builder()
    .applicationRuntimeId("ApplicationRuntimeId4")
    .supportedDpuSizes(Arrays.asList(
        17,
        18
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



