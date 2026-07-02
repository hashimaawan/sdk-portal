# Object Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk9iamVjdFR5cGU

Metadata about the Kubernetes API object the diagnostic is reported on.

*This model accepts additional fields of type Object.*


# Class Name

`ObjectType`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Kind` | `String` | Optional | The kind of Kubernetes API object | String getKind() | setKind(String kind) |
| `Name` | `String` | Optional | Name of the object | String getName() | setName(String name) |
| `Namespace` | `String` | Optional | The namespace the object resides in the cluster. | String getNamespace() | setNamespace(String namespace) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ObjectType;
import java.io.IOException;

ObjectType objectType = new ObjectType.Builder()
    .kind("config map")
    .name("foo")
    .namespace("kube-system")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



