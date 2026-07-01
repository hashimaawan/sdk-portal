# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Currency` | `String` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 | String getCurrency() | setCurrency(String currency) |
| `FloatingIp` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month | FloatingIp4 getFloatingIp() | setFloatingIp(FloatingIp4 floatingIp) |
| `FloatingIps` | [`List<FloatingIp5>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type | List<FloatingIp5> getFloatingIps() | setFloatingIps(List<FloatingIp5> floatingIps) |
| `Image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/image-3.md) | Required | The cost of Image per GB/month | Image3 getImage() | setImage(Image3 image) |
| `LoadBalancerTypes` | [`List<LoadBalancerType6>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type | List<LoadBalancerType6> getLoadBalancerTypes() | setLoadBalancerTypes(List<LoadBalancerType6> loadBalancerTypes) |
| `PrimaryIps` | [`List<PrimaryIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location | List<PrimaryIp> getPrimaryIps() | setPrimaryIps(List<PrimaryIp> primaryIps) |
| `ServerBackup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage | ServerBackup getServerBackup() | setServerBackup(ServerBackup serverBackup) |
| `ServerTypes` | [`List<ServerTypes2>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type | List<ServerTypes2> getServerTypes() | setServerTypes(List<ServerTypes2> serverTypes) |
| `Traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/traffic.md) | Required | The cost of additional traffic per TB | Traffic getTraffic() | setTraffic(Traffic traffic) |
| `VatRate` | `String` | Required | The VAT rate used for calculating prices with VAT | String getVatRate() | setVatRate(String vatRate) |
| `Volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/volume.md) | Required | The cost of Volume per GB/month | Volume getVolume() | setVolume(Volume volume) |


# Example

```java
import cloud.hetzner.api.models.FloatingIp4;
import cloud.hetzner.api.models.FloatingIp5;
import cloud.hetzner.api.models.Image3;
import cloud.hetzner.api.models.LoadBalancerType6;
import cloud.hetzner.api.models.Price6;
import cloud.hetzner.api.models.Price7;
import cloud.hetzner.api.models.Price8;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly6;
import cloud.hetzner.api.models.PriceHourly7;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.PriceMonthly6;
import cloud.hetzner.api.models.PriceMonthly7;
import cloud.hetzner.api.models.PriceMonthly8;
import cloud.hetzner.api.models.PriceMonthly9;
import cloud.hetzner.api.models.PricePerGbMonth;
import cloud.hetzner.api.models.PricePerTb;
import cloud.hetzner.api.models.Pricing;
import cloud.hetzner.api.models.PrimaryIp;
import cloud.hetzner.api.models.ServerBackup;
import cloud.hetzner.api.models.ServerTypes2;
import cloud.hetzner.api.models.Traffic;
import cloud.hetzner.api.models.Type48Enum;
import cloud.hetzner.api.models.Type49Enum;
import cloud.hetzner.api.models.Volume;
import java.util.Arrays;

Pricing pricing = new Pricing.Builder(
    "EUR",
    new FloatingIp4.Builder(
        new PriceMonthly6.Builder(
            "1.1900000000000000",
            "1.0000000000"
        )
        .build()
    )
    .build(),
    Arrays.asList(
        new FloatingIp5.Builder(
            Arrays.asList(
                new Price6.Builder(
                    "fsn1",
                    new PriceMonthly7.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build()
                )
                .build()
            ),
            Type48Enum.IPV4
        )
        .build()
    ),
    new Image3.Builder(
        new PricePerGbMonth.Builder(
            "1.1900000000000000",
            "1.0000000000"
        )
        .build()
    )
    .build(),
    Arrays.asList(
        new LoadBalancerType6.Builder(
            1D,
            "lb11",
            Arrays.asList(
                new Price7.Builder(
                    "fsn1",
                    new PriceHourly6.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build(),
                    new PriceMonthly8.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build()
                )
                .build()
            )
        )
        .build()
    ),
    Arrays.asList(
        new PrimaryIp.Builder(
            Arrays.asList(
                new Price8.Builder(
                    "fsn1",
                    new PriceHourly7.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build(),
                    new PriceMonthly9.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build()
                )
                .build()
            ),
            Type49Enum.IPV4
        )
        .build()
    ),
    new ServerBackup.Builder(
        "20.0000000000"
    )
    .build(),
    Arrays.asList(
        new ServerTypes2.Builder(
            4D,
            "cx11",
            Arrays.asList(
                new Price9.Builder(
                    "fsn1",
                    new PriceHourly8.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build(),
                    new PriceMonthly10.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build()
                )
                .build()
            )
        )
        .build()
    ),
    new Traffic.Builder(
        new PricePerTb.Builder(
            "1.1900000000000000",
            "1.0000000000"
        )
        .build()
    )
    .build(),
    "19.000000",
    new Volume.Builder(
        new PricePerGbMonth.Builder(
            "1.1900000000000000",
            "1.0000000000"
        )
        .build()
    )
    .build()
)
.build();
```



