# Domain

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRvbWFpbg

*This model accepts additional fields of type Object.*


# Class Name

`Domain`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Domain` | `String` | Required | The hostname for the domain<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `253`, *Pattern*: `^((xn--)?[a-zA-Z0-9]+(-[a-zA-Z0-9]+)*\.)+[a-zA-Z]{2,}\.?$` | String getDomain() | setDomain(String domain) |
| `MinimumTlsVersion` | [`MinimumTlsVersion`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/minimum-tls-version.md) | Optional | The minimum version of TLS a client application can use to access resources for the domain.  Must be one of the following values wrapped within quotations: `"1.2"` or `"1.3"`.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` | MinimumTlsVersion getMinimumTlsVersion() | setMinimumTlsVersion(MinimumTlsVersion minimumTlsVersion) |
| `Type` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-1.md) | Optional | - DEFAULT: The default `.ondigitalocean.app` domain assigned to this app<br>- PRIMARY: The primary domain for this app that is displayed as the default in the control panel, used in bindable environment variables, and any other places that reference an app's live URL. Only one domain may be set as primary.<br>- ALIAS: A non-primary domain<br><br>**Default**: `Type1.UNSPECIFIED` | Type1 getType() | setType(Type1 type) |
| `Wildcard` | `Boolean` | Optional | Indicates whether the domain includes all sub-domains, in addition to the given domain | Boolean getWildcard() | setWildcard(Boolean wildcard) |
| `Zone` | `String` | Optional | Optional. If the domain uses DigitalOcean DNS and you would like App<br>Platform to automatically manage it for you, set this to the name of the<br>domain on your account.<br><br>For example, If the domain you are adding is `app.domain.com`, the zone<br>could be `domain.com`. | String getZone() | setZone(String zone) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Domain;
import com.digitalocean.api.models.MinimumTlsVersion;
import com.digitalocean.api.models.Type1;
import java.io.IOException;

Domain domain = new Domain.Builder(
    "app.example.com"
)
.minimumTlsVersion(MinimumTlsVersion.ENUM_13)
.type(Type1.DEFAULT)
.wildcard(true)
.zone("example.com")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



