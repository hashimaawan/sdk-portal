# V2 Registry Garbage Collection Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbiUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistryGarbageCollectionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GarbageCollection` | [`GarbageCollection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/garbage-collection.md) | Optional | - | GarbageCollection getGarbageCollection() | setGarbageCollection(GarbageCollection garbageCollection) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.GarbageCollection;
import com.digitalocean.api.models.Status15;
import com.digitalocean.api.models.V2RegistryGarbageCollectionResponse;
import java.io.IOException;

V2RegistryGarbageCollectionResponse v2RegistryGarbageCollectionResponse = new V2RegistryGarbageCollectionResponse.Builder()
    .garbageCollection(new GarbageCollection.Builder()
        .blobsDeleted(40)
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .freedBytes(86)
        .registryName("registry_name6")
        .status(Status15.SUCCEEDED)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



