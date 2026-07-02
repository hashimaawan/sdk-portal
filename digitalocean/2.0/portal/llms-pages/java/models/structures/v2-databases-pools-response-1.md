# V2 Databases Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesPoolsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Pool` | [`Pool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pool.md) | Required | - | Pool getPool() | setPool(Pool pool) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.Pool;
import com.digitalocean.api.models.PrivateConnection;
import com.digitalocean.api.models.V2DatabasesPoolsResponse1;
import java.io.IOException;

V2DatabasesPoolsResponse1 v2DatabasesPoolsResponse1 = new V2DatabasesPoolsResponse1.Builder(
    new Pool.Builder(
        "defaultdb",
        "transaction",
        "backend-pool",
        10
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
    .user("doadmin")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



