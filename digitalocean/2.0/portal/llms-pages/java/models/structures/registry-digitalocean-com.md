# Registry Digitalocean Com

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlZ2lzdHJ5RGlnaXRhbG9jZWFuQ29t

*This model accepts additional fields of type Object.*


# Class Name

`RegistryDigitaloceanCom`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Auth` | `String` | Optional | A base64 encoded string containing credentials for the container registry. | String getAuth() | setAuth(String auth) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.RegistryDigitaloceanCom;
import java.io.IOException;

RegistryDigitaloceanCom registryDigitaloceanCom = new RegistryDigitaloceanCom.Builder()
    .auth("YjdkMDNhNjk0N2IyMTdlZmI2ZjNlYzNiZDM1MDQ1ODI6YjdkMDNhNjk0N2IyMTdlZmI2ZjNlYzNiZDM1MDQ1ODIK")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



