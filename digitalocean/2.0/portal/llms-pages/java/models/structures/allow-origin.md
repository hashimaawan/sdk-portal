# Allow Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFsbG93T3JpZ2lu

*This model accepts additional fields of type Object.*


# Class Name

`AllowOrigin`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Exact` | `String` | Optional | Exact string match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getExact() | setExact(String exact) |
| `Prefix` | `String` | Optional | Prefix-based match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getPrefix() | setPrefix(String prefix) |
| `Regex` | `String` | Optional | RE2 style regex-based match. Only 1 of `exact`, `prefix`, or `regex` must be set. For more information about RE2 syntax, see: https://github.com/google/re2/wiki/Syntax<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getRegex() | setRegex(String regex) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AllowOrigin;
import java.io.IOException;

AllowOrigin allowOrigin = new AllowOrigin.Builder()
    .exact("https://www.example.com")
    .prefix("https://www.example.com")
    .regex("^.*example.com")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



