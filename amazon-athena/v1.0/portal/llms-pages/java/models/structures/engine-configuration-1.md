# Engine Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type Object.*


# Class Name

`EngineConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CoordinatorDpuSize` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` | Integer getCoordinatorDpuSize() | setCoordinatorDpuSize(Integer coordinatorDpuSize) |
| `MaxConcurrentDpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` | int getMaxConcurrentDpus() | setMaxConcurrentDpus(int maxConcurrentDpus) |
| `DefaultExecutorDpuSize` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` | Integer getDefaultExecutorDpuSize() | setDefaultExecutorDpuSize(Integer defaultExecutorDpuSize) |
| `AdditionalConfigs` | [`AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/additional-configs.md) | Optional | - | AdditionalConfigs getAdditionalConfigs() | setAdditionalConfigs(AdditionalConfigs additionalConfigs) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AdditionalConfigs;
import com.amazonaws.useast1.athena.models.EngineConfiguration1;
import java.io.IOException;

EngineConfiguration1 engineConfiguration1 = new EngineConfiguration1.Builder(
    214
)
.coordinatorDpuSize(1)
.defaultExecutorDpuSize(1)
.additionalConfigs(new AdditionalConfigs.Builder()
    .additionalProperty("exampleAdditionalProperty", "AdditionalConfigs_additionalProperties5")
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



