# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type Object.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Registry` | `String` | Optional | The registry name. Must be left empty for the `DOCR` registry type. | String getRegistry() | setRegistry(String registry) |
| `RegistryType` | [`RegistryType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/registry-type.md) | Optional | - DOCKER_HUB: The DockerHub container registry type.<br>- DOCR: The DigitalOcean container registry type. | RegistryType getRegistryType() | setRegistryType(RegistryType registryType) |
| `Repository` | `String` | Optional | The repository name. | String getRepository() | setRepository(String repository) |
| `Tag` | `String` | Optional | The repository tag. Defaults to `latest` if not provided.<br><br>**Default**: `"latest"` | String getTag() | setTag(String tag) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Image;
import com.digitalocean.api.models.RegistryType;
import java.io.IOException;

Image image = new Image.Builder()
    .registry("registry.hub.docker.com")
    .registryType(RegistryType.DOCR)
    .repository("origin/master")
    .tag("latest")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



