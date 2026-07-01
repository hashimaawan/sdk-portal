# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-type.md) | Optional | - | LoadBalancerType getLoadBalancerType() | setLoadBalancerType(LoadBalancerType loadBalancerType) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancerType;
import cloud.hetzner.api.models.LoadBalancerTypesResponse1;
import cloud.hetzner.api.models.Price;
import cloud.hetzner.api.models.PriceHourly;
import cloud.hetzner.api.models.PriceMonthly;
import java.util.Arrays;

LoadBalancerTypesResponse1 loadBalancerTypesResponse1 = new LoadBalancerTypesResponse1.Builder()
    .loadBalancerType(new LoadBalancerType.Builder(
        "deprecated2",
        "description4",
        205.06D,
        211.64D,
        136.32D,
        199.18D,
        152.52D,
        "name6",
        Arrays.asList(
            new Price.Builder(
                "location8",
                new PriceHourly.Builder(
                    "gross4",
                    "net2"
                )
                .build(),
                new PriceMonthly.Builder(
                    "gross2",
                    "net0"
                )
                .build()
            )
            .build(),
            new Price.Builder(
                "location8",
                new PriceHourly.Builder(
                    "gross4",
                    "net2"
                )
                .build(),
                new PriceMonthly.Builder(
                    "gross2",
                    "net0"
                )
                .build()
            )
            .build(),
            new Price.Builder(
                "location8",
                new PriceHourly.Builder(
                    "gross4",
                    "net2"
                )
                .build(),
                new PriceMonthly.Builder(
                    "gross2",
                    "net0"
                )
                .build()
            )
            .build()
        )
    )
    .build())
    .build();
```



