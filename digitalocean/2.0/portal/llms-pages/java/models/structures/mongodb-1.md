# Mongodb 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk1vbmdvZGIx

*This model accepts additional fields of type Object.*


# Class Name

`Mongodb1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EndOfAvailability` | `String` | Optional | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. | String getEndOfAvailability() | setEndOfAvailability(String endOfAvailability) |
| `EndOfLife` | `String` | Optional | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. | String getEndOfLife() | setEndOfLife(String endOfLife) |
| `Version` | `String` | Optional | The engine version. | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Mongodb1;
import java.io.IOException;

Mongodb1 mongodb1 = new Mongodb1.Builder()
    .endOfAvailability("2023-05-09T00:00:00Z")
    .endOfLife("2023-11-09T00:00:00Z")
    .version("8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



