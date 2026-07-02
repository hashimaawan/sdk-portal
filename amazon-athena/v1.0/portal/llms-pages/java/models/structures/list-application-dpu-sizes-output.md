# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0


# Class Name

`ListApplicationDPUSizesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApplicationDPUSizes` | [`List<ApplicationDPUSizes>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/application-dpu-sizes.md) | Optional | - | List<ApplicationDPUSizes> getApplicationDPUSizes() | setApplicationDPUSizes(List<ApplicationDPUSizes> applicationDPUSizes) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.ApplicationDPUSizes;
import com.amazonaws.useast1.athena.models.ListApplicationDPUSizesOutput;
import java.util.Arrays;

ListApplicationDPUSizesOutput listApplicationDPUSizesOutput = new ListApplicationDPUSizesOutput.Builder()
    .applicationDPUSizes(Arrays.asList(
        new ApplicationDPUSizes.Builder()
            .applicationRuntimeId("ApplicationRuntimeId0")
            .supportedDPUSizes(Arrays.asList(
                113,
                114
            ))
            .build(),
        new ApplicationDPUSizes.Builder()
            .applicationRuntimeId("ApplicationRuntimeId0")
            .supportedDPUSizes(Arrays.asList(
                113,
                114
            ))
            .build()
    ))
    .nextToken("NextToken0")
    .build();
```



