# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlVzZWRCeQ


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of resource referenced | int getId() | setId(int id) |
| `Type` | `String` | Required | Type of resource referenced | String getType() | setType(String type) |


# Example

```java
import cloud.hetzner.api.models.UsedBy;

UsedBy usedBy = new UsedBy.Builder(
    4711,
    "load_balancer"
)
.build();
```



