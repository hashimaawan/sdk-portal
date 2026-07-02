# Filters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkZpbHRlcnM


# Class Name

`Filters`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getName() | setName(String name) |


# Example

```java
import com.amazonaws.useast1.athena.models.Filters;

Filters filters = new Filters.Builder()
    .name("Name0")
    .build();
```



