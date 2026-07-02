# V2 Load Balancers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2LoadBalancersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancers` | [`List<LoadBalancer1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/load-balancer-1.md) | Optional | - | List<LoadBalancer1> getLoadBalancers() | setLoadBalancers(List<LoadBalancer1> loadBalancers) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Algorithm;
import com.digitalocean.api.models.EntryProtocol;
import com.digitalocean.api.models.ForwardingRule;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.LoadBalancer1;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.TargetProtocol;
import com.digitalocean.api.models.V2LoadBalancersResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2LoadBalancersResponse v2LoadBalancersResponse = new V2LoadBalancersResponse.Builder(
    new Meta.Builder(
        1
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.loadBalancers(Arrays.asList(
        new LoadBalancer1.Builder(
            Arrays.asList(
                new ForwardingRule.Builder(
                    220,
                    EntryProtocol.HTTP2,
                    104,
                    TargetProtocol.HTTPS
                )
                .certificateId("certificate_id4")
                .tlsPassthrough(false)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
        )
        .algorithm(Algorithm.ROUND_ROBIN)
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .disableLetsEncryptDnsRecords(false)
        .enableBackendKeepalive(false)
        .enableProxyProtocol(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("last6")
                .next("next2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



