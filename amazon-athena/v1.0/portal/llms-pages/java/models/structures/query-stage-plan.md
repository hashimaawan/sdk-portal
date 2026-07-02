# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu

*This model accepts additional fields of type Object.*


# Class Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Identifier` | `String` | Optional | - | String getIdentifier() | setIdentifier(String identifier) |
| `Children` | [`List<QueryStagePlanNode>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-stage-plan-node.md) | Optional | - | List<QueryStagePlanNode> getChildren() | setChildren(List<QueryStagePlanNode> children) |
| `RemoteSources` | `List<String>` | Optional | - | List<String> getRemoteSources() | setRemoteSources(List<String> remoteSources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.QueryStagePlan;
import com.amazonaws.useast1.athena.models.QueryStagePlanNode;
import java.io.IOException;
import java.util.Arrays;

QueryStagePlan queryStagePlan = new QueryStagePlan.Builder()
    .name("Name0")
    .identifier("Identifier6")
    .children(Arrays.asList(
        new QueryStagePlanNode.Builder()
            .name("Name6")
            .identifier("Identifier2")
            .children(Arrays.asList(
                new QueryStagePlanNode.Builder()
                    .build()
            ))
            .remoteSources(Arrays.asList(
                "RemoteSources4",
                "RemoteSources5",
                "RemoteSources6"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .remoteSources(Arrays.asList(
        "RemoteSources8",
        "RemoteSources9",
        "RemoteSources0"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



