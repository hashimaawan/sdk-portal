# Auths

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkF1dGhz

*This model accepts additional fields of type Object.*


# Class Name

`Auths`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RegistryDigitaloceanCom` | [`RegistryDigitaloceanCom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/registry-digitalocean-com.md) | Optional | - | RegistryDigitaloceanCom getRegistryDigitaloceanCom() | setRegistryDigitaloceanCom(RegistryDigitaloceanCom registryDigitaloceanCom) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Auths;
import com.digitalocean.api.models.RegistryDigitaloceanCom;
import java.io.IOException;

Auths auths = new Auths.Builder()
    .registryDigitaloceanCom(new RegistryDigitaloceanCom.Builder()
        .auth("auth0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



