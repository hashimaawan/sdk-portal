# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU


# Class Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Deprecated` | `String` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) | String getDeprecated() | setDeprecated(String deprecated) |
| `Description` | `String` | Required | Description of the Load Balancer type | String getDescription() | setDescription(String description) |
| `Id` | `double` | Required | ID of the Load Balancer type | double getId() | setId(double id) |
| `MaxAssignedCertificates` | `double` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer | double getMaxAssignedCertificates() | setMaxAssignedCertificates(double maxAssignedCertificates) |
| `MaxConnections` | `double` | Required | Number of maximum simultaneous open connections | double getMaxConnections() | setMaxConnections(double maxConnections) |
| `MaxServices` | `double` | Required | Number of services a Load Balancer of this type can have | double getMaxServices() | setMaxServices(double maxServices) |
| `MaxTargets` | `double` | Required | Number of targets a single Load Balancer can have | double getMaxTargets() | setMaxTargets(double maxTargets) |
| `Name` | `String` | Required | Unique identifier of the Load Balancer type | String getName() | setName(String name) |
| `Prices` | [`List<Price>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/price.md) | Required | Prices in different network zones | List<Price> getPrices() | setPrices(List<Price> prices) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancerType;
import cloud.hetzner.api.models.Price;
import cloud.hetzner.api.models.PriceHourly;
import cloud.hetzner.api.models.PriceMonthly;
import java.util.Arrays;

LoadBalancerType loadBalancerType = new LoadBalancerType.Builder(
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
            .build(),
            new PriceMonthly.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .build()
        )
        .build()
    )
)
.build();
```



