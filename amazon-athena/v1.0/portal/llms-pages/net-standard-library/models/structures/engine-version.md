# Engine Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24

The Athena engine version for running queries, or the PySpark engine version for running sessions.


# Class Name

`EngineVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SelectedEngineVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `EffectiveEngineVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```csharp
using AmazonAthena.Standard.Models;

EngineVersion engineVersion = new EngineVersion
{
    SelectedEngineVersion = "SelectedEngineVersion0",
    EffectiveEngineVersion = "EffectiveEngineVersion0",
};
```



