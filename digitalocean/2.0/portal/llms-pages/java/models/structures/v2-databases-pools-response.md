# V2 Databases Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesPoolsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Pools` | [`List<Pool>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pool.md) | Optional, Read-only | An array of connection pool objects. | List<Pool> getPools() | setPools(List<Pool> pools) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.Pool;
import com.digitalocean.api.models.PrivateConnection;
import com.digitalocean.api.models.V2DatabasesPoolsResponse;
import java.io.IOException;
import java.util.Arrays;

V2DatabasesPoolsResponse v2DatabasesPoolsResponse = new V2DatabasesPoolsResponse.Builder()
    .pools(Arrays.asList(
        new Pool.Builder(
            "db2",
            "mode0",
            "name2",
            68
        )
        .connection(new Connection.Builder()
                .database("database2")
                .host("host0")
                .password("password2")
                .port(174)
                .ssl(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .privateConnection(new PrivateConnection.Builder()
                .database("database4")
                .host("host4")
                .password("password8")
                .port(228)
                .ssl(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .user("user2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



