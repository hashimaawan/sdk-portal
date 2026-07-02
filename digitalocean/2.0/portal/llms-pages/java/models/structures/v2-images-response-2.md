# V2 Images Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type Object.*


# Class Name

`V2ImagesResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/image-1.md) | Required | - | Image1 getImage() | setImage(Image1 image) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Distribution;
import com.digitalocean.api.models.Image1;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.Status7;
import com.digitalocean.api.models.Type9;
import com.digitalocean.api.models.V2ImagesResponse2;
import java.io.IOException;
import java.util.Arrays;

V2ImagesResponse2 v2ImagesResponse2 = new V2ImagesResponse2.Builder(
    new Image1.Builder()
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-05-04T22:23:02Z"))
        .description("description6")
        .distribution(Distribution.UBUNTU)
        .errorMessage("error_message8")
        .id(7555620)
        .minDiskSize(20)
        .name("Nifty New Snapshot")
        .mPublic(true)
        .regions(Arrays.asList(
            Region2.NYC1,
            Region2.NYC2
        ))
        .sizeGigabytes(2.34D)
        .slug("nifty1")
        .status(Status7.NEW)
        .tags(Arrays.asList(
            "base-image",
            "prod"
        ))
        .type(Type9.SNAPSHOT)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



