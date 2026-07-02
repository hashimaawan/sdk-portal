# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.

*This model accepts additional fields of type Object.*


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getName() | setName(String name) |
| `Type` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` | String getType() | setType(String type) |
| `Comment` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` | String getComment() | setComment(String comment) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Column;
import java.io.IOException;

Column column = new Column.Builder(
    "Name6"
)
.type("Type6")
.comment("Comment2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



