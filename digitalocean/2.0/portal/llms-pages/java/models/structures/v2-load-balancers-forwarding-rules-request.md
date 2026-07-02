# V2 Load Balancers Forwarding Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMEZvcndhcmRpbmclMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2LoadBalancersForwardingRulesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ForwardingRules` | [`List<ForwardingRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/forwarding-rule.md) | Required | **Constraints**: *Minimum Items*: `1` | List<ForwardingRule> getForwardingRules() | setForwardingRules(List<ForwardingRule> forwardingRules) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.EntryProtocol;
import com.digitalocean.api.models.ForwardingRule;
import com.digitalocean.api.models.TargetProtocol;
import com.digitalocean.api.models.V2LoadBalancersForwardingRulesRequest;
import java.io.IOException;
import java.util.Arrays;

V2LoadBalancersForwardingRulesRequest v2LoadBalancersForwardingRulesRequest = new V2LoadBalancersForwardingRulesRequest.Builder(
    Arrays.asList(
        new ForwardingRule.Builder(
            443,
            EntryProtocol.HTTPS,
            80,
            TargetProtocol.HTTP
        )
        .certificateId("892071a0-bb95-49bc-8021-3afd67a210bf")
        .tlsPassthrough(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



