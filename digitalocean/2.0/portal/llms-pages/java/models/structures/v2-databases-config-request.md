# V2 Databases Config Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesConfigRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Config` | [`V2DatabasesConfigRequestConfig`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/v2-databases-config-request-config.md) | Optional | This is a container for any-of cases. | V2DatabasesConfigRequestConfig getConfig() | setConfig(V2DatabasesConfigRequestConfig config) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Config;
import com.digitalocean.api.models.V2DatabasesConfigRequest;
import com.digitalocean.api.models.containers.V2DatabasesConfigRequestConfig;
import java.io.IOException;

V2DatabasesConfigRequest v2DatabasesConfigRequest = new V2DatabasesConfigRequest.Builder()
    .config(V2DatabasesConfigRequestConfig.fromConfig(
        new Config.Builder()
            .backupHour(23)
            .backupMinute(59)
            .binlogRetentionPeriod(600D)
            .connectTimeout(196)
            .defaultTimeZone("default_time_zone8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



