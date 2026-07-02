# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueries` | [`List<NamedQuery>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/named-query.md) | Optional | - | List<NamedQuery> getNamedQueries() | setNamedQueries(List<NamedQuery> namedQueries) |
| `UnprocessedNamedQueryIds` | [`List<UnprocessedNamedQueryId>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/unprocessed-named-query-id.md) | Optional | - | List<UnprocessedNamedQueryId> getUnprocessedNamedQueryIds() | setUnprocessedNamedQueryIds(List<UnprocessedNamedQueryId> unprocessedNamedQueryIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.BatchGetNamedQueryOutput;
import com.amazonaws.useast1.athena.models.NamedQuery;
import com.amazonaws.useast1.athena.models.UnprocessedNamedQueryId;
import java.io.IOException;
import java.util.Arrays;

BatchGetNamedQueryOutput batchGetNamedQueryOutput = new BatchGetNamedQueryOutput.Builder()
    .namedQueries(Arrays.asList(
        new NamedQuery.Builder(
            "Name2",
            "Database0",
            "QueryString4"
        )
        .description("Description4")
        .namedQueryId("NamedQueryId0")
        .workGroup("WorkGroup4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new NamedQuery.Builder(
            "Name2",
            "Database0",
            "QueryString4"
        )
        .description("Description4")
        .namedQueryId("NamedQueryId0")
        .workGroup("WorkGroup4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new NamedQuery.Builder(
            "Name2",
            "Database0",
            "QueryString4"
        )
        .description("Description4")
        .namedQueryId("NamedQueryId0")
        .workGroup("WorkGroup4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
    .unprocessedNamedQueryIds(Arrays.asList(
        new UnprocessedNamedQueryId.Builder()
            .namedQueryId("NamedQueryId4")
            .errorCode("ErrorCode6")
            .errorMessage("ErrorMessage4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new UnprocessedNamedQueryId.Builder()
            .namedQueryId("NamedQueryId4")
            .errorCode("ErrorCode6")
            .errorMessage("ErrorMessage4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



