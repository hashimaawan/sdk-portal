# V2 Registry Garbage Collections Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistryGarbageCollectionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GarbageCollections` | [`List<GarbageCollection>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/garbage-collection.md) | Optional | - | List<GarbageCollection> getGarbageCollections() | setGarbageCollections(List<GarbageCollection> garbageCollections) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.GarbageCollection;
import com.digitalocean.api.models.Status15;
import com.digitalocean.api.models.V2RegistryGarbageCollectionsResponse;
import java.io.IOException;
import java.util.Arrays;

V2RegistryGarbageCollectionsResponse v2RegistryGarbageCollectionsResponse = new V2RegistryGarbageCollectionsResponse.Builder()
    .garbageCollections(Arrays.asList(
        new GarbageCollection.Builder()
            .blobsDeleted(26)
            .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .freedBytes(100)
            .registryName("registry_name2")
            .status(Status15.REQUESTED)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



