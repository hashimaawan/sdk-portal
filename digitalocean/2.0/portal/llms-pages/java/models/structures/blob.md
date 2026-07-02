# Blob

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkJsb2I

*This model accepts additional fields of type Object.*


# Class Name

`Blob`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CompressedSizeBytes` | `Integer` | Optional | The compressed size of the blob in bytes. | Integer getCompressedSizeBytes() | setCompressedSizeBytes(Integer compressedSizeBytes) |
| `Digest` | `String` | Optional | The digest of the blob | String getDigest() | setDigest(String digest) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Blob;
import java.io.IOException;

Blob blob = new Blob.Builder()
    .compressedSizeBytes(2803255)
    .digest("sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



