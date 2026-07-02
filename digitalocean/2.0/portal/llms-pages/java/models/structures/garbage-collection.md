# Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkdhcmJhZ2VDb2xsZWN0aW9u

*This model accepts additional fields of type Object.*


# Class Name

`GarbageCollection`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BlobsDeleted` | `Integer` | Optional | The number of blobs deleted as a result of this garbage collection. | Integer getBlobsDeleted() | setBlobsDeleted(Integer blobsDeleted) |
| `CreatedAt` | `LocalDateTime` | Optional | The time the garbage collection was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `FreedBytes` | `Integer` | Optional | The number of bytes freed as a result of this garbage collection. | Integer getFreedBytes() | setFreedBytes(Integer freedBytes) |
| `RegistryName` | `String` | Optional | The name of the container registry. | String getRegistryName() | setRegistryName(String registryName) |
| `Status` | [`Status15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-15.md) | Optional | The current status of this garbage collection. | Status15 getStatus() | setStatus(Status15 status) |
| `UpdatedAt` | `LocalDateTime` | Optional | The time the garbage collection was last updated. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `Uuid` | `String` | Optional | A string specifying the UUID of the garbage collection. | String getUuid() | setUuid(String uuid) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.GarbageCollection;
import com.digitalocean.api.models.Status15;
import java.io.IOException;

GarbageCollection garbageCollection = new GarbageCollection.Builder()
    .blobsDeleted(42)
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-10-30T21:03:24Z"))
    .freedBytes(667)
    .registryName("example")
    .status(Status15.REQUESTED)
    .updatedAt(DateTimeHelper.fromRfc8601DateTime("2020-10-30T21:03:44Z"))
    .uuid("eff0feee-49c7-4e8f-ba5c-a320c109c8a8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



