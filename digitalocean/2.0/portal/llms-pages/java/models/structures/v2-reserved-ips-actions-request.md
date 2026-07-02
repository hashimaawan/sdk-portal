# V2 Reserved Ips Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2ReservedIpsActionsRequest`


# Inherits From

[`BaseType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/base-type.md)


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DropletId` | `int` | Required | The ID of the Droplet that the reserved IP will be assigned to. | int getDropletId() | setDropletId(int dropletId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2ReservedIpsActionsRequest;
import java.io.IOException;

V2ReservedIpsActionsRequest v2ReservedIpsActionsRequest = new V2ReservedIpsActionsRequest.Builder(
    758604968
)
.type("V2 Reserved Ips Actions Request")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

*This model accepts additional fields of type Object.*


# Class Name

`BaseType`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | `String` | Optional | - | String getType() | setType(String type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.BaseType;
import java.io.IOException;

BaseType baseType = new BaseType.Builder()
    .type("BaseType")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



