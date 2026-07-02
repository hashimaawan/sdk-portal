# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x


# Class Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SelectedEngineVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getSelectedEngineVersion() | setSelectedEngineVersion(String selectedEngineVersion) |
| `EffectiveEngineVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getEffectiveEngineVersion() | setEffectiveEngineVersion(String effectiveEngineVersion) |


# Example

```java
import com.amazonaws.useast1.athena.models.EngineVersion1;

EngineVersion1 engineVersion1 = new EngineVersion1.Builder()
    .selectedEngineVersion("SelectedEngineVersion2")
    .effectiveEngineVersion("EffectiveEngineVersion8")
    .build();
```



