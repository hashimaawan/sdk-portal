# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlJlc291cmNl


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Type` | `String` | Required | Type of resource referenced | String getType() | setType(String type) |


# Example

```java
import cloud.hetzner.api.models.Resource;

Resource resource = new Resource.Builder(
    42,
    "server"
)
.build();
```



