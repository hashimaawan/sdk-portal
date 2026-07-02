# V2 Databases Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9wdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesOptionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Options` | [`Options`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/options.md) | Optional | - | Options getOptions() | setOptions(Options options) |
| `VersionAvailability` | [`VersionAvailability`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/version-availability.md) | Optional | - | VersionAvailability getVersionAvailability() | setVersionAvailability(VersionAvailability versionAvailability) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Layout;
import com.digitalocean.api.models.Mongodb;
import com.digitalocean.api.models.Mongodb1;
import com.digitalocean.api.models.Mysql;
import com.digitalocean.api.models.Options;
import com.digitalocean.api.models.Pg;
import com.digitalocean.api.models.Redis;
import com.digitalocean.api.models.V2DatabasesOptionsResponse;
import com.digitalocean.api.models.VersionAvailability;
import java.io.IOException;
import java.util.Arrays;

V2DatabasesOptionsResponse v2DatabasesOptionsResponse = new V2DatabasesOptionsResponse.Builder()
    .options(new Options.Builder()
        .mongodb(new Mongodb.Builder()
            .regions(Arrays.asList(
                "regions3",
                "regions4"
            ))
            .versions(Arrays.asList(
                "versions3",
                "versions4"
            ))
            .layouts(Arrays.asList(
                new Layout.Builder()
                    .numNodes(190)
                    .sizes(Arrays.asList(
                        "sizes2",
                        "sizes3"
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new Layout.Builder()
                    .numNodes(190)
                    .sizes(Arrays.asList(
                        "sizes2",
                        "sizes3"
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .mysql(new Mysql.Builder()
            .regions(Arrays.asList(
                "regions9",
                "regions0",
                "regions1"
            ))
            .versions(Arrays.asList(
                "versions9",
                "versions0",
                "versions1"
            ))
            .layouts(Arrays.asList(
                new Layout.Builder()
                    .numNodes(190)
                    .sizes(Arrays.asList(
                        "sizes2",
                        "sizes3"
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new Layout.Builder()
                    .numNodes(190)
                    .sizes(Arrays.asList(
                        "sizes2",
                        "sizes3"
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new Layout.Builder()
                    .numNodes(190)
                    .sizes(Arrays.asList(
                        "sizes2",
                        "sizes3"
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .pg(new Pg.Builder()
            .regions(Arrays.asList(
                "regions3"
            ))
            .versions(Arrays.asList(
                "versions3"
            ))
            .layouts(Arrays.asList(
                new Layout.Builder()
                    .numNodes(190)
                    .sizes(Arrays.asList(
                        "sizes2",
                        "sizes3"
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .redis(new Redis.Builder()
            .regions(Arrays.asList(
                "regions7"
            ))
            .versions(Arrays.asList(
                "versions7"
            ))
            .layouts(Arrays.asList(
                new Layout.Builder()
                    .numNodes(190)
                    .sizes(Arrays.asList(
                        "sizes2",
                        "sizes3"
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .versionAvailability(new VersionAvailability.Builder()
        .mongodb(Arrays.asList(
            new Mongodb1.Builder()
                .endOfAvailability("end_of_availability4")
                .endOfLife("end_of_life4")
                .version("version4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Mongodb1.Builder()
                .endOfAvailability("end_of_availability4")
                .endOfLife("end_of_life4")
                .version("version4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .mysql(Arrays.asList(
            new Mongodb1.Builder()
                .endOfAvailability("end_of_availability0")
                .endOfLife("end_of_life0")
                .version("version0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Mongodb1.Builder()
                .endOfAvailability("end_of_availability0")
                .endOfLife("end_of_life0")
                .version("version0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .pg(Arrays.asList(
            new Mongodb1.Builder()
                .endOfAvailability("end_of_availability4")
                .endOfLife("end_of_life4")
                .version("version4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .redis(Arrays.asList(
            new Mongodb1.Builder()
                .endOfAvailability("end_of_availability8")
                .endOfLife("end_of_life8")
                .version("version8")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



