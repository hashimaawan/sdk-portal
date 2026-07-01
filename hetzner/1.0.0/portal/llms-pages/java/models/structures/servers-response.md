# Servers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`ServersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `Servers` | [`List<Server18>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-18.md) | Required | - | List<Server18> getServers() | setServers(List<Server18> servers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CpuType;
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Datacenter6;
import cloud.hetzner.api.models.DnsPtr8;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.Ipv44;
import cloud.hetzner.api.models.Ipv64;
import cloud.hetzner.api.models.Iso2;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.OsFlavor;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.PlacementGroupNullable;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.PrivateNet4;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Protection20;
import cloud.hetzner.api.models.PublicNet4;
import cloud.hetzner.api.models.Server18;
import cloud.hetzner.api.models.ServerPublicNetFirewall;
import cloud.hetzner.api.models.ServerType1;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.ServersResponse;
import cloud.hetzner.api.models.Status24;
import cloud.hetzner.api.models.Status72;
import cloud.hetzner.api.models.Status73;
import cloud.hetzner.api.models.StorageType;
import cloud.hetzner.api.models.Type22;
import cloud.hetzner.api.models.Type26;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

ServersResponse serversResponse = new ServersResponse.Builder(
    Arrays.asList(
        new Server18.Builder(
            "22-02",
            "2016-01-30T23:55:00+00:00",
            new Datacenter6.Builder(
                "Falkenstein DC Park 8",
                42,
                new Location.Builder(
                    "Falkenstein",
                    "DE",
                    "Falkenstein DC Park 1",
                    1D,
                    50.47612D,
                    12.370071D,
                    "fsn1",
                    "eu-central"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
                "fsn1-dc8",
                new ServerTypes.Builder(
                    Arrays.asList(
                        1D,
                        2D,
                        3D
                    ),
                    Arrays.asList(
                        1D,
                        2D,
                        3D
                    ),
                    Arrays.asList(
                        1D,
                        2D,
                        3D
                    )
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            42,
            new Image.Builder(
                null,
                "2016-01-30T23:55:00+00:00",
                new CreatedFrom.Builder(
                    1,
                    "Server"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
                null,
                "2018-02-28T00:00:00+00:00",
                "Ubuntu 20.04 Standard 64 bit",
                10D,
                42,
                2.3D,
                new LinkedHashMap<String, String>() {{
                    put("key0", "labels4");
                }},
                "ubuntu-20.04",
                OsFlavor.UBUNTU,
                "20.04",
                new Protection.Builder(
                    false
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
                Status24.UNAVAILABLE,
                Type22.SNAPSHOT
            )
            .rapidDeploy(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            654321D,
            123456D,
            new Iso2.Builder(
                "2018-02-28T00:00:00+00:00",
                "FreeBSD 11.0 x64",
                42,
                "FreeBSD-11.0-RELEASE-amd64-dvd1",
                Type26.ENUM_PUBLIC
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new LinkedHashMap<String, String>() {{
                put("key0", "labels0");
            }},
            false,
            "my-resource",
            123456D,
            50D,
            Arrays.asList(
                new PrivateNet4.Builder()
                    .aliasIps(Arrays.asList(
                        "alias_ips4"
                    ))
                    .ip("10.0.0.2")
                    .macAddress("86:00:ff:2a:7d:e1")
                    .network(4711)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ),
            new Protection20.Builder(
                false,
                false
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new PublicNet4.Builder(
                Arrays.asList(
                    478
                ),
                new Ipv44.Builder(
                    false,
                    "server01.example.com",
                    "1.2.3.4"
                )
                .id(42)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
                new Ipv64.Builder(
                    false,
                    Arrays.asList(
                        new DnsPtr8.Builder(
                            "server.example.com",
                            "2001:db8::1"
                        )
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                    ),
                    "2001:db8::/64"
                )
                .id(42)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
            .firewalls(Arrays.asList(
                    new ServerPublicNetFirewall.Builder()
                        .id(250)
                        .status(Status72.APPLIED)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ServerPublicNetFirewall.Builder()
                        .id(250)
                        .status(Status72.APPLIED)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            false,
            new ServerType1.Builder(
                1D,
                CpuType.SHARED,
                false,
                "CX11",
                25D,
                1,
                1D,
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
                ),
                StorageType.LOCAL
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            Status73.STARTING
        )
        .loadBalancers(Arrays.asList(
                128,
                129,
                130
            ))
        .placementGroup(new PlacementGroupNullable.Builder(
                "created8",
                236,
                new LinkedHashMap<String, String>() {{
                    put("key0", "labels4");
                }},
                "name8",
                Arrays.asList(
                    251,
                    252,
                    253
                ),
                "type2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .volumes(Arrays.asList(
                177
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.meta(new Meta.Builder(
        new Pagination.Builder(
            77.7D,
            209.18D,
            17.58D,
            13.34D,
            50.02D,
            206.64D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



