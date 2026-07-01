# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVzZWRCeQ

*This model accepts additional fields of type Object.*


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of resource referenced | int getId() | setId(int id) |
| `Type` | `String` | Required | Type of resource referenced | String getType() | setType(String type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.UsedBy;
import java.io.IOException;

UsedBy usedBy = new UsedBy.Builder(
    4711,
    "load_balancer"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



