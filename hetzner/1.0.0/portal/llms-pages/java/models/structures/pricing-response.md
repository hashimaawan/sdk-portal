# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/pricing.md) | Required | - | Pricing getPricing() | setPricing(Pricing pricing) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
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
import cloud.hetzner.api.models.PricingResponse;
import cloud.hetzner.api.models.PrimaryIp;
import cloud.hetzner.api.models.ServerBackup;
import cloud.hetzner.api.models.ServerTypes2;
import cloud.hetzner.api.models.Traffic;
import cloud.hetzner.api.models.Type48;
import cloud.hetzner.api.models.Type49;
import cloud.hetzner.api.models.Volume;
import java.io.IOException;
import java.util.Arrays;

PricingResponse pricingResponse = new PricingResponse.Builder(
    new Pricing.Builder(
        "EUR",
        new FloatingIp4.Builder(
            new PriceMonthly6.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
                ),
                Type48.IPV4
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        new Image3.Builder(
            new PricePerGbMonth.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                        new PriceMonthly8.Builder(
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
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                        new PriceMonthly9.Builder(
                            "1.1900000000000000",
                            "1.0000000000"
                        )
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
                ),
                Type49.IPV4
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        new ServerBackup.Builder(
            "20.0000000000"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                        new PriceMonthly10.Builder(
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
        ),
        new Traffic.Builder(
            new PricePerTb.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "19.000000",
        new Volume.Builder(
            new PricePerGbMonth.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



