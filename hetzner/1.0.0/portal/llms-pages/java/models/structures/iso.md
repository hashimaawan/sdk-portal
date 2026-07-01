# Iso

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRklzbw

*This model accepts additional fields of type Object.*


# Class Name

`Iso`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Deprecated` | `String` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. | String getDeprecated() | setDeprecated(String deprecated) |
| `Description` | `String` | Required | Description of the ISO | String getDescription() | setDescription(String description) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Name` | `String` | Required | Unique identifier of the ISO. Only set for public ISOs | String getName() | setName(String name) |
| `Type` | [`Type26`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-26.md) | Required | Type of the ISO | Type26 getType() | setType(Type26 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Iso;
import cloud.hetzner.api.models.Type26;
import java.io.IOException;

Iso iso = new Iso.Builder(
    "2018-02-28T00:00:00+00:00",
    "FreeBSD 11.0 x64",
    42,
    "FreeBSD-11.0-RELEASE-amd64-dvd1",
    Type26.ENUM_PUBLIC
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



