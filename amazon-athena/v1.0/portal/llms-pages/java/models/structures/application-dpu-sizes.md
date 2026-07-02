# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.


# Class Name

`ApplicationDPUSizes`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApplicationRuntimeId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getApplicationRuntimeId() | setApplicationRuntimeId(String applicationRuntimeId) |
| `SupportedDPUSizes` | `List<Integer>` | Optional | - | List<Integer> getSupportedDPUSizes() | setSupportedDPUSizes(List<Integer> supportedDPUSizes) |


# Example

```java
import com.amazonaws.useast1.athena.models.ApplicationDPUSizes;
import java.util.Arrays;

ApplicationDPUSizes applicationDPUSizes = new ApplicationDPUSizes.Builder()
    .applicationRuntimeId("ApplicationRuntimeId2")
    .supportedDPUSizes(Arrays.asList(
        57
    ))
    .build();
```



