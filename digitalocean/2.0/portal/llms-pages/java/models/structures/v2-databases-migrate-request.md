# V2 Databases Migrate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME1pZ3JhdGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesMigrateRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Region` | `String` | Required | A slug identifier for the region to which the database cluster will be migrated. | String getRegion() | setRegion(String region) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2DatabasesMigrateRequest;
import java.io.IOException;

V2DatabasesMigrateRequest v2DatabasesMigrateRequest = new V2DatabasesMigrateRequest.Builder(
    "lon1"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



