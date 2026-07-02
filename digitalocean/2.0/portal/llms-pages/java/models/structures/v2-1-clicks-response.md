# V2 1 Clicks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V21ClicksResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `M1Clicks` | [`List<M1Click>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/1-click.md) | Optional | - | List<M1Click> getM1Clicks() | setM1Clicks(List<M1Click> m1Clicks) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.M1Click;
import com.digitalocean.api.models.V21ClicksResponse;
import java.io.IOException;
import java.util.Arrays;

V21ClicksResponse v21ClicksResponse = new V21ClicksResponse.Builder()
    .m1Clicks(Arrays.asList(
        new M1Click.Builder(
            "slug8",
            "type2"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new M1Click.Builder(
            "slug8",
            "type2"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



