# Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk9wdGlvbnM

*This model accepts additional fields of type Object.*


# Class Name

`Options`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Mongodb` | [`Mongodb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mongodb.md) | Optional | - | Mongodb getMongodb() | setMongodb(Mongodb mongodb) |
| `Mysql` | [`Mysql`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mysql.md) | Optional | - | Mysql getMysql() | setMysql(Mysql mysql) |
| `Pg` | [`Pg`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pg.md) | Optional | - | Pg getPg() | setPg(Pg pg) |
| `Redis` | [`Redis`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/redis.md) | Optional | - | Redis getRedis() | setRedis(Redis redis) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Layout;
import com.digitalocean.api.models.Mongodb;
import com.digitalocean.api.models.Mysql;
import com.digitalocean.api.models.Options;
import com.digitalocean.api.models.Pg;
import com.digitalocean.api.models.Redis;
import java.io.IOException;
import java.util.Arrays;

Options options = new Options.Builder()
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
    .build();
```



