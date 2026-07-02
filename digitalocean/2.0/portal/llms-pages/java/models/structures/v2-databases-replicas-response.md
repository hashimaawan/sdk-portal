# V2 Databases Replicas Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcGxpY2FzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesReplicasResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Replicas` | [`List<Replica>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/replica.md) | Optional | - | List<Replica> getReplicas() | setReplicas(List<Replica> replicas) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.PrivateConnection;
import com.digitalocean.api.models.Replica;
import com.digitalocean.api.models.V2DatabasesReplicasResponse;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2DatabasesReplicasResponse v2DatabasesReplicasResponse = new V2DatabasesReplicasResponse.Builder()
    .replicas(Arrays.asList(
        new Replica.Builder(
            "name6"
        )
        .connection(new Connection.Builder()
                .database("database2")
                .host("host0")
                .password("password2")
                .port(174)
                .ssl(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .id(UUID.fromString("000022b6-0000-0000-0000-000000000000"))
        .privateConnection(new PrivateConnection.Builder()
                .database("database4")
                .host("host4")
                .password("password8")
                .port(228)
                .ssl(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .privateNetworkUuid("private_network_uuid6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Replica.Builder(
            "name6"
        )
        .connection(new Connection.Builder()
                .database("database2")
                .host("host0")
                .password("password2")
                .port(174)
                .ssl(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .id(UUID.fromString("000022b6-0000-0000-0000-000000000000"))
        .privateConnection(new PrivateConnection.Builder()
                .database("database4")
                .host("host4")
                .password("password8")
                .port(228)
                .ssl(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .privateNetworkUuid("private_network_uuid6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



