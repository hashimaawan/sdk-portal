# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.


# Class Name

`QueryStagePlanNode`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Identifier` | `String` | Optional | - | String getIdentifier() | setIdentifier(String identifier) |
| `Children` | [`List<QueryStagePlanNode>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-stage-plan-node.md) | Optional | - | List<QueryStagePlanNode> getChildren() | setChildren(List<QueryStagePlanNode> children) |
| `RemoteSources` | `List<String>` | Optional | - | List<String> getRemoteSources() | setRemoteSources(List<String> remoteSources) |


# Example

```java
import com.amazonaws.useast1.athena.models.QueryStagePlanNode;
import java.util.Arrays;

QueryStagePlanNode queryStagePlanNode = new QueryStagePlanNode.Builder()
    .name("Name4")
    .identifier("Identifier0")
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
            .build()
    ))
    .remoteSources(Arrays.asList(
        "RemoteSources2",
        "RemoteSources3",
        "RemoteSources4"
    ))
    .build();
```



