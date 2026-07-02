# Version Availability

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlZlcnNpb25BdmFpbGFiaWxpdHk

*This model accepts additional fields of type Object.*


# Class Name

`VersionAvailability`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Mongodb` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | List<Mongodb1> getMongodb() | setMongodb(List<Mongodb1> mongodb) |
| `Mysql` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | List<Mongodb1> getMysql() | setMysql(List<Mongodb1> mysql) |
| `Pg` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | List<Mongodb1> getPg() | setPg(List<Mongodb1> pg) |
| `Redis` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | List<Mongodb1> getRedis() | setRedis(List<Mongodb1> redis) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Mongodb1;
import com.digitalocean.api.models.VersionAvailability;
import java.io.IOException;
import java.util.Arrays;

VersionAvailability versionAvailability = new VersionAvailability.Builder()
    .mongodb(Arrays.asList(
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
            .build()
    ))
    .pg(Arrays.asList(
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
            .build(),
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
            .build(),
        new Mongodb1.Builder()
            .endOfAvailability("end_of_availability8")
            .endOfLife("end_of_life8")
            .version("version8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



