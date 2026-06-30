# Iso

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRklzbw


# Class Name

`Iso`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Deprecated` | `String` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. | String getDeprecated() | setDeprecated(String deprecated) |
| `Description` | `String` | Required | Description of the ISO | String getDescription() | setDescription(String description) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Name` | `String` | Required | Unique identifier of the ISO. Only set for public ISOs | String getName() | setName(String name) |
| `Type` | [`Type26Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-26.md) | Required | Type of the ISO | Type26Enum getType() | setType(Type26Enum type) |


# Example

```java
import cloud.hetzner.api.models.Iso;
import cloud.hetzner.api.models.Type26Enum;

Iso iso = new Iso.Builder(
    "2018-02-28T00:00:00+00:00",
    "FreeBSD 11.0 x64",
    42,
    "FreeBSD-11.0-RELEASE-amd64-dvd1",
    Type26Enum.ENUM_PUBLIC
)
.build();
```



