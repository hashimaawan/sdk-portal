# List Named Queries Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListNamedQueriesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueryIds` | `List<String>` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | List<String> getNamedQueryIds() | setNamedQueryIds(List<String> namedQueryIds) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ListNamedQueriesOutput;
import java.io.IOException;
import java.util.Arrays;

ListNamedQueriesOutput listNamedQueriesOutput = new ListNamedQueriesOutput.Builder()
    .namedQueryIds(Arrays.asList(
        "NamedQueryIds5",
        "NamedQueryIds4",
        "NamedQueryIds3"
    ))
    .nextToken("NextToken2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



