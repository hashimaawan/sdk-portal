# V2 Databases Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEZpcmV3YWxsJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesFirewallResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Rules` | [`List<Rule1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/rule-1.md) | Optional | - | List<Rule1> getRules() | setRules(List<Rule1> rules) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Rule1;
import com.digitalocean.api.models.Type7;
import com.digitalocean.api.models.V2DatabasesFirewallResponse;
import java.io.IOException;
import java.util.Arrays;

V2DatabasesFirewallResponse v2DatabasesFirewallResponse = new V2DatabasesFirewallResponse.Builder()
    .rules(Arrays.asList(
        new Rule1.Builder(
            Type7.IP_ADDR,
            "value0"
        )
        .clusterUuid("cluster_uuid4")
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .uuid("uuid4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



