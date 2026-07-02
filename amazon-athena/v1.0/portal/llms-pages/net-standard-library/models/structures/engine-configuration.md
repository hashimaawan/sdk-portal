# Engine Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24

Contains data processing unit (DPU) configuration settings and parameter mappings for a notebook engine.


# Class Name

`EngineConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CoordinatorDpuSize` | `int?` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `MaxConcurrentDpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `DefaultExecutorDpuSize` | `int?` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `AdditionalConfigs` | [`AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/additional-configs.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

EngineConfiguration engineConfiguration = new EngineConfiguration
{
    MaxConcurrentDpus = 194,
    CoordinatorDpuSize = 1,
    DefaultExecutorDpuSize = 1,
    AdditionalConfigs = new AdditionalConfigs
    {
    },
};
```



