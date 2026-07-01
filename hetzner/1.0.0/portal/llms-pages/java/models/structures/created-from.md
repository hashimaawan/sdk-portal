# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from

*This model accepts additional fields of type Object.*


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server the Image was created from | int getId() | setId(int id) |
| `Name` | `String` | Required | Server name at the time the Image was created | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreatedFrom;
import java.io.IOException;

CreatedFrom createdFrom = new CreatedFrom.Builder(
    1,
    "Server"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



