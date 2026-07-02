# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroups` | [`List<WorkGroupSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` | List<WorkGroupSummary> getWorkGroups() | setWorkGroups(List<WorkGroupSummary> workGroups) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.EngineVersion1;
import com.amazonaws.useast1.athena.models.ListWorkGroupsOutput;
import com.amazonaws.useast1.athena.models.WorkGroupState1;
import com.amazonaws.useast1.athena.models.WorkGroupSummary;
import java.io.IOException;
import java.util.Arrays;

ListWorkGroupsOutput listWorkGroupsOutput = new ListWorkGroupsOutput.Builder()
    .workGroups(Arrays.asList(
        new WorkGroupSummary.Builder()
            .name("Name4")
            .state(WorkGroupState1.ENABLED)
            .description("Description0")
            .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .engineVersion(new EngineVersion1.Builder()
                .selectedEngineVersion("SelectedEngineVersion4")
                .effectiveEngineVersion("EffectiveEngineVersion6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new WorkGroupSummary.Builder()
            .name("Name4")
            .state(WorkGroupState1.ENABLED)
            .description("Description0")
            .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .engineVersion(new EngineVersion1.Builder()
                .selectedEngineVersion("SelectedEngineVersion4")
                .effectiveEngineVersion("EffectiveEngineVersion6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new WorkGroupSummary.Builder()
            .name("Name4")
            .state(WorkGroupState1.ENABLED)
            .description("Description0")
            .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .engineVersion(new EngineVersion1.Builder()
                .selectedEngineVersion("SelectedEngineVersion4")
                .effectiveEngineVersion("EffectiveEngineVersion6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .nextToken("NextToken2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



