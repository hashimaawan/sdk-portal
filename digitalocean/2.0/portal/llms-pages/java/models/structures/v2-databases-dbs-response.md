# V2 Databases Dbs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMERicyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesDbsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Dbs` | [`List<Db>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/db.md) | Optional | - | List<Db> getDbs() | setDbs(List<Db> dbs) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Db;
import com.digitalocean.api.models.V2DatabasesDbsResponse;
import java.io.IOException;
import java.util.Arrays;

V2DatabasesDbsResponse v2DatabasesDbsResponse = new V2DatabasesDbsResponse.Builder()
    .dbs(Arrays.asList(
        new Db.Builder(
            "name6"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Db.Builder(
            "name6"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Db.Builder(
            "name6"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



