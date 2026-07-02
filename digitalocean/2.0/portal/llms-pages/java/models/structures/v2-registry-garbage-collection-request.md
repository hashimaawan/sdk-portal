# V2 Registry Garbage Collection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistryGarbageCollectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cancel` | `Boolean` | Optional | A boolean value indicating that the garbage collection should be cancelled. | Boolean getCancel() | setCancel(Boolean cancel) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2RegistryGarbageCollectionRequest;
import java.io.IOException;

V2RegistryGarbageCollectionRequest v2RegistryGarbageCollectionRequest = new V2RegistryGarbageCollectionRequest.Builder()
    .cancel(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



