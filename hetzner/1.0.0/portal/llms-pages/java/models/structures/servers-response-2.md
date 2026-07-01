# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type Object.*


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-18.md) | Optional | - | Server18 getServer() | setServer(Server18 server) |
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
import cloud.hetzner.api.models.OsFlavor;
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
import cloud.hetzner.api.models.ServersResponse2;
import cloud.hetzner.api.models.Status24;
import cloud.hetzner.api.models.Status72;
import cloud.hetzner.api.models.Status73;
import cloud.hetzner.api.models.StorageType;
import cloud.hetzner.api.models.Type22;
import cloud.hetzner.api.models.Type26;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

ServersResponse2 serversResponse2 = new ServersResponse2.Builder()
    .server(new Server18.Builder(
        "backup_window2",
        "created4",
        new Datacenter6.Builder(
            "description0",
            200,
            new Location.Builder(
                "city6",
                "country8",
                "description6",
                187.14D,
                194.62D,
                59.18D,
                "name4",
                "network_zone2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "name0",
            new ServerTypes.Builder(
                Arrays.asList(
                    23.74D
                ),
                Arrays.asList(
                    201.65D,
                    201.66D
                ),
                Arrays.asList(
                    69.52D,
                    69.53D,
                    69.54D
                )
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        14,
        new Image.Builder(
            186,
            "created6",
            new CreatedFrom.Builder(
                60,
                "name6"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "deleted4",
            "deprecated8",
            "description6",
            244.18D,
            128,
            141.34D,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels4");
            }},
            "name6",
            OsFlavor.DEBIAN,
            "os_version4",
            new Protection.Builder(
                false
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            Status24.UNAVAILABLE,
            Type22.APP
        )
        .rapidDeploy(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        123.68D,
        151.82D,
        new Iso2.Builder(
            "deprecated0",
            "description2",
            66,
            "name8",
            Type26.ENUM_PUBLIC
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new LinkedHashMap<String, String>() {{
            put("key0", "labels0");
            put("key1", "labels9");
        }},
        false,
        "name4",
        129.6D,
        19.88D,
        Arrays.asList(
            new PrivateNet4.Builder()
                .aliasIps(Arrays.asList(
                    "alias_ips4"
                ))
                .ip("ip6")
                .macAddress("mac_address0")
                .network(154)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new PrivateNet4.Builder()
                .aliasIps(Arrays.asList(
                    "alias_ips4"
                ))
                .ip("ip6")
                .macAddress("mac_address0")
                .network(154)
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
                54,
                55,
                56
            ),
            new Ipv44.Builder(
                false,
                "dns_ptr4",
                "ip2"
            )
            .id(104)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Ipv64.Builder(
                false,
                Arrays.asList(
                    new DnsPtr8.Builder(
                        "dns_ptr0",
                        "ip6"
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                    new DnsPtr8.Builder(
                        "dns_ptr0",
                        "ip6"
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
                ),
                "ip0"
            )
            .id(8)
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
            12.84D,
            CpuType.SHARED,
            false,
            "description0",
            14.32D,
            30,
            21.2D,
            "name0",
            Arrays.asList(
                new Price9.Builder(
                    "location8",
                    new PriceHourly8.Builder(
                        "gross4",
                        "net2"
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                    new PriceMonthly10.Builder(
                        "gross2",
                        "net0"
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
            144,
            143,
            142
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
            91,
            92
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



