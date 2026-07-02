# Engine Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24

Contains data processing unit (DPU) configuration settings and parameter mappings for a notebook engine.


# Class Name

`EngineConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CoordinatorDpuSize` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` | Integer getCoordinatorDpuSize() | setCoordinatorDpuSize(Integer coordinatorDpuSize) |
| `MaxConcurrentDpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` | int getMaxConcurrentDpus() | setMaxConcurrentDpus(int maxConcurrentDpus) |
| `DefaultExecutorDpuSize` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` | Integer getDefaultExecutorDpuSize() | setDefaultExecutorDpuSize(Integer defaultExecutorDpuSize) |
| `AdditionalConfigs` | [`AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/additional-configs.md) | Optional | - | AdditionalConfigs getAdditionalConfigs() | setAdditionalConfigs(AdditionalConfigs additionalConfigs) |


# Example

```java
import com.amazonaws.useast1.athena.models.AdditionalConfigs;
import com.amazonaws.useast1.athena.models.EngineConfiguration;

EngineConfiguration engineConfiguration = new EngineConfiguration.Builder(
    194
)
.coordinatorDpuSize(1)
.defaultExecutorDpuSize(1)
.additionalConfigs(new AdditionalConfigs.Builder()
        .build())
.build();
```



