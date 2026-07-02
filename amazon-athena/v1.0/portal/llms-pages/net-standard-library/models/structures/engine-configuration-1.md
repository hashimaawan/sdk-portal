# Engine Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type object.*


# Class Name

`EngineConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CoordinatorDpuSize` | `int?` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `MaxConcurrentDpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `DefaultExecutorDpuSize` | `int?` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `AdditionalConfigs` | [`AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/additional-configs.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

EngineConfiguration1 engineConfiguration1 = new EngineConfiguration1
{
    MaxConcurrentDpus = 214,
    CoordinatorDpuSize = 1,
    DefaultExecutorDpuSize = 1,
    AdditionalConfigs = new AdditionalConfigs
    {
        ["exampleAdditionalProperty"] = "AdditionalConfigs_additionalProperties5",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



