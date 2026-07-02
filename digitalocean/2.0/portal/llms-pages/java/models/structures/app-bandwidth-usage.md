# App Bandwidth Usage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFwcEJhbmR3aWR0aFVzYWdl

Bandwidth usage for an app.

*This model accepts additional fields of type Object.*


# Class Name

`AppBandwidthUsage`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AppId` | `String` | Optional | The ID of the app. | String getAppId() | setAppId(String appId) |
| `BandwidthBytes` | `String` | Optional | The used bandwidth amount in bytes. | String getBandwidthBytes() | setBandwidthBytes(String bandwidthBytes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AppBandwidthUsage;
import java.io.IOException;

AppBandwidthUsage appBandwidthUsage = new AppBandwidthUsage.Builder()
    .appId("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf")
    .bandwidthBytes("513668")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



