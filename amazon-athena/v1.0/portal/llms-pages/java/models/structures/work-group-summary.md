# Work Group Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRldvcmtHcm91cFN1bW1hcnk

The summary information for the workgroup, which includes its name, state, description, and the date and time it was created.

*This model accepts additional fields of type Object.*


# Class Name

`WorkGroupSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getName() | setName(String name) |
| `State` | [`WorkGroupState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/work-group-state-1.md) | Optional | - | WorkGroupState1 getState() | setState(WorkGroupState1 state) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `CreationTime` | `LocalDateTime` | Optional | - | LocalDateTime getCreationTime() | setCreationTime(LocalDateTime creationTime) |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-version-1.md) | Optional | - | EngineVersion1 getEngineVersion() | setEngineVersion(EngineVersion1 engineVersion) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.EngineVersion1;
import com.amazonaws.useast1.athena.models.WorkGroupState1;
import com.amazonaws.useast1.athena.models.WorkGroupSummary;
import java.io.IOException;

WorkGroupSummary workGroupSummary = new WorkGroupSummary.Builder()
    .name("Name4")
    .state(WorkGroupState1.ENABLED)
    .description("Description8")
    .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .engineVersion(new EngineVersion1.Builder()
        .selectedEngineVersion("SelectedEngineVersion4")
        .effectiveEngineVersion("EffectiveEngineVersion6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



