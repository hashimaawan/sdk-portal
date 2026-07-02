# Links 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxpbmtzMQ

*This model accepts additional fields of type Object.*


# Class Name

`Links1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/action-1.md) | Optional | - | List<Action1> getActions() | setActions(List<Action1> actions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Action1;
import com.digitalocean.api.models.Links1;
import java.io.IOException;
import java.util.Arrays;

Links1 links1 = new Links1.Builder()
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
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



