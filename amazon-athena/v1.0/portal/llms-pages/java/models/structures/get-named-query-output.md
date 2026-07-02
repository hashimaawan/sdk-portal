# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQuery` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/named-query-1.md) | Optional | - | NamedQuery1 getNamedQuery() | setNamedQuery(NamedQuery1 namedQuery) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetNamedQueryOutput;
import com.amazonaws.useast1.athena.models.NamedQuery1;
import java.io.IOException;

GetNamedQueryOutput getNamedQueryOutput = new GetNamedQueryOutput.Builder()
    .namedQuery(new NamedQuery1.Builder(
        "Name0",
        "Database8",
        "QueryString2"
    )
    .description("Description6")
    .namedQueryId("NamedQueryId2")
    .workGroup("WorkGroup2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



