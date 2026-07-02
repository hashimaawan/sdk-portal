# V2 Databases Upgrade Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVwZ3JhZGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesUpgradeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Version` | `String` | Optional | A string representing the version of the database engine in use for the cluster. | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2DatabasesUpgradeRequest;
import java.io.IOException;

V2DatabasesUpgradeRequest v2DatabasesUpgradeRequest = new V2DatabasesUpgradeRequest.Builder()
    .version("10")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



