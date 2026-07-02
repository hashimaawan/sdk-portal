# V2 Registry Docker Credentials Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRG9ja2VyJTI1MjBDcmVkZW50aWFscyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistryDockerCredentialsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Auths` | [`Auths`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/auths.md) | Optional | - | Auths getAuths() | setAuths(Auths auths) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Auths;
import com.digitalocean.api.models.RegistryDigitaloceanCom;
import com.digitalocean.api.models.V2RegistryDockerCredentialsResponse;
import java.io.IOException;

V2RegistryDockerCredentialsResponse v2RegistryDockerCredentialsResponse = new V2RegistryDockerCredentialsResponse.Builder()
    .auths(new Auths.Builder()
        .registryDigitaloceanCom(new RegistryDigitaloceanCom.Builder()
            .auth("auth0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



