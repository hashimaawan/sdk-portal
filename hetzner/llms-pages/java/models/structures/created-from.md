# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server the Image was created from | int getId() | setId(int id) |
| `Name` | `String` | Required | Server name at the time the Image was created | String getName() | setName(String name) |


# Example

```java
import cloud.hetzner.api.models.CreatedFrom;

CreatedFrom createdFrom = new CreatedFrom.Builder(
    1,
    "Server"
)
.build();
```



