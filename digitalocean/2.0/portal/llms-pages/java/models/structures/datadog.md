# Datadog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFkb2c

DataDog configuration.

*This model accepts additional fields of type Object.*


# Class Name

`Datadog`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApiKey` | `String` | Required | Datadog API key. | String getApiKey() | setApiKey(String apiKey) |
| `Endpoint` | `String` | Optional | Datadog HTTP log intake endpoint. | String getEndpoint() | setEndpoint(String endpoint) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Datadog;
import java.io.IOException;

Datadog datadog = new Datadog.Builder(
    "abcdefghijklmnopqrstuvwxyz0123456789"
)
.endpoint("https://mydatadogendpoint.com")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



