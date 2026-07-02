# Links 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxpbmtzMw

*This model accepts additional fields of type Object.*


# Class Name

`Links3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/action-1.md) | Optional | - | List<Action1> getActions() | setActions(List<Action1> actions) |
| `Droplets` | [`List<Action1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/action-1.md) | Optional | - | List<Action1> getDroplets() | setDroplets(List<Action1> droplets) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Action1;
import com.digitalocean.api.models.Links3;
import java.io.IOException;
import java.util.Arrays;

Links3 links3 = new Links3.Builder()
    .actions(Arrays.asList(
        new Action1.Builder()
            .href("href0")
            .id(154)
            .rel("rel4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Action1.Builder()
            .href("href0")
            .id(154)
            .rel("rel4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .droplets(Arrays.asList(
        new Action1.Builder()
            .href("href2")
            .id(232)
            .rel("rel6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Action1.Builder()
            .href("href2")
            .id(232)
            .rel("rel6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Action1.Builder()
            .href("href2")
            .id(232)
            .rel("rel6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



