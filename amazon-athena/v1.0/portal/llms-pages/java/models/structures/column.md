# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getName() | setName(String name) |
| `Type` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` | String getType() | setType(String type) |
| `Comment` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` | String getComment() | setComment(String comment) |


# Example

```java
import com.amazonaws.useast1.athena.models.Column;

Column column = new Column.Builder(
    "Name6"
)
.type("Type6")
.comment("Comment2")
.build();
```



