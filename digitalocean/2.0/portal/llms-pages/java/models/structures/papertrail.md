# Papertrail

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBhcGVydHJhaWw

Papertrail configuration.

*This model accepts additional fields of type Object.*


# Class Name

`Papertrail`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Endpoint` | `String` | Required | Papertrail syslog endpoint. | String getEndpoint() | setEndpoint(String endpoint) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Papertrail;
import java.io.IOException;

Papertrail papertrail = new Papertrail.Builder(
    "https://mypapertrailendpoint.com"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



