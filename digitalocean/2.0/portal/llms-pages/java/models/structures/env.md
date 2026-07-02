# Env

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkVudg

*This model accepts additional fields of type Object.*


# Class Name

`Env`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Required | The variable name<br><br>**Constraints**: *Pattern*: `^[_A-Za-z][_A-Za-z0-9]*$` | String getKey() | setKey(String key) |
| `Scope` | [`Scope`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/scope.md) | Optional | - RUN_TIME: Made available only at run-time<br>- BUILD_TIME: Made available only at build-time<br>- RUN_AND_BUILD_TIME: Made available at both build and run-time<br><br>**Default**: `Scope.RUN_AND_BUILD_TIME` | Scope getScope() | setScope(Scope scope) |
| `Type` | [`Type2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-2.md) | Optional | - GENERAL: A plain-text environment variable<br>- SECRET: A secret encrypted environment variable<br><br>**Default**: `Type2.GENERAL` | Type2 getType() | setType(Type2 type) |
| `Value` | `String` | Optional | The value. If the type is `SECRET`, the value will be encrypted on first submission. On following submissions, the encrypted value should be used. | String getValue() | setValue(String value) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Env;
import com.digitalocean.api.models.Scope;
import com.digitalocean.api.models.Type2;
import java.io.IOException;

Env env = new Env.Builder(
    "BASE_URL"
)
.scope(Scope.BUILD_TIME)
.type(Type2.GENERAL)
.value("http://example.com")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



