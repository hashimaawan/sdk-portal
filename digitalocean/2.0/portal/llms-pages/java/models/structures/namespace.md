# Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk5hbWVzcGFjZQ

*This model accepts additional fields of type Object.*


# Class Name

`Namespace`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApiHost` | `String` | Optional | The namespace's API hostname. Each function in a namespace is provided an endpoint at the namespace's hostname. | String getApiHost() | setApiHost(String apiHost) |
| `CreatedAt` | `String` | Optional | UTC time string. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Key` | `String` | Optional | A random alpha numeric string. This key is used in conjunction with the namespace's UUID to authenticate<br>a user to use the namespace via `doctl`, DigitalOcean's official CLI. | String getKey() | setKey(String key) |
| `Label` | `String` | Optional | The namespace's unique name. | String getLabel() | setLabel(String label) |
| `Namespace` | `String` | Optional | A unique string format of UUID with a prefix fn-. | String getNamespace() | setNamespace(String namespace) |
| `Region` | `String` | Optional | The namespace's datacenter region. | String getRegion() | setRegion(String region) |
| `UpdatedAt` | `String` | Optional | UTC time string. | String getUpdatedAt() | setUpdatedAt(String updatedAt) |
| `Uuid` | `String` | Optional | The namespace's Universally Unique Identifier. | String getUuid() | setUuid(String uuid) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Namespace;
import java.io.IOException;

Namespace namespace = new Namespace.Builder()
    .apiHost("https://api_host.io")
    .createdAt("2022-09-14T04:16:45Z")
    .key("d1zcd455h01mqjfs4s2eaewyejehi5f2uj4etqq3h7cera8iwkub6xg5of1wdde2")
    .label("my namespace")
    .namespace("fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
    .region("nyc1")
    .updatedAt("2022-09-14T04:16:45Z")
    .uuid("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



