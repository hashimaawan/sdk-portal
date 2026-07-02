# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.


# Class Name

`FilterDefinition`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getName() | setName(String name) |


# Example

```java
import com.amazonaws.useast1.athena.models.FilterDefinition;

FilterDefinition filterDefinition = new FilterDefinition.Builder()
    .name("Name2")
    .build();
```



