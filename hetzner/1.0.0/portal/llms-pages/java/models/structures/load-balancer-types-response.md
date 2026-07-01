# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancerTypes` | [`List<LoadBalancerType>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-type.md) | Required | - | List<LoadBalancerType> getLoadBalancerTypes() | setLoadBalancerTypes(List<LoadBalancerType> loadBalancerTypes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LoadBalancerType;
import cloud.hetzner.api.models.LoadBalancerTypesResponse;
import cloud.hetzner.api.models.Price;
import cloud.hetzner.api.models.PriceHourly;
import cloud.hetzner.api.models.PriceMonthly;
import java.io.IOException;
import java.util.Arrays;

LoadBalancerTypesResponse loadBalancerTypesResponse = new LoadBalancerTypesResponse.Builder(
    Arrays.asList(
        new LoadBalancerType.Builder(
            "2016-01-30T23:50:00+00:00",
            "LB11",
            1D,
            10D,
            20000D,
            5D,
            25D,
            "lb11",
            Arrays.asList(
                new Price.Builder(
                    "fsn1",
                    new PriceHourly.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                    new PriceMonthly.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



