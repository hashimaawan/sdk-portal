# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x

*This model accepts additional fields of type Object.*


# Class Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SelectedEngineVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getSelectedEngineVersion() | setSelectedEngineVersion(String selectedEngineVersion) |
| `EffectiveEngineVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getEffectiveEngineVersion() | setEffectiveEngineVersion(String effectiveEngineVersion) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.EngineVersion1;
import java.io.IOException;

EngineVersion1 engineVersion1 = new EngineVersion1.Builder()
    .selectedEngineVersion("SelectedEngineVersion2")
    .effectiveEngineVersion("EffectiveEngineVersion8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



