# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x

*This model accepts additional fields of type object.*


# Class Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SelectedEngineVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `EffectiveEngineVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

EngineVersion1 engineVersion1 = new EngineVersion1
{
    SelectedEngineVersion = "SelectedEngineVersion2",
    EffectiveEngineVersion = "EffectiveEngineVersion8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



