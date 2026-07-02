# Engine Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24

The Athena engine version for running queries, or the PySpark engine version for running sessions.


# Class Name

`EngineVersion`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SelectedEngineVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getSelectedEngineVersion() | setSelectedEngineVersion(String selectedEngineVersion) |
| `EffectiveEngineVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getEffectiveEngineVersion() | setEffectiveEngineVersion(String effectiveEngineVersion) |


# Example

```java
import com.amazonaws.useast1.athena.models.EngineVersion;

EngineVersion engineVersion = new EngineVersion.Builder()
    .selectedEngineVersion("SelectedEngineVersion0")
    .effectiveEngineVersion("EffectiveEngineVersion0")
    .build();
```



