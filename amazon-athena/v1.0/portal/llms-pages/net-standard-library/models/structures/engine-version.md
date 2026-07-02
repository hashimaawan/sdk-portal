# Engine Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24

The Athena engine version for running queries, or the PySpark engine version for running sessions.

*This model accepts additional fields of type object.*


# Class Name

`EngineVersion`


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

EngineVersion engineVersion = new EngineVersion
{
    SelectedEngineVersion = "SelectedEngineVersion0",
    EffectiveEngineVersion = "EffectiveEngineVersion0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



