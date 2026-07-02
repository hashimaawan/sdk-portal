# Batch Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeUlucHV0

Contains an array of named query IDs.

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueryIds` | `List<String>` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | List<String> getNamedQueryIds() | setNamedQueryIds(List<String> namedQueryIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.BatchGetNamedQueryInput;
import java.io.IOException;
import java.util.Arrays;

BatchGetNamedQueryInput batchGetNamedQueryInput = new BatchGetNamedQueryInput.Builder(
    Arrays.asList(
        "NamedQueryIds3",
        "NamedQueryIds4"
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



