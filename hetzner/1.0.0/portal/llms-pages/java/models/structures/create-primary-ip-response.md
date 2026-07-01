# Create Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`CreatePrimaryIpResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `PrimaryIp` | [`PrimaryIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-ip-1.md) | Required | - | PrimaryIp1 getPrimaryIp() | setPrimaryIp(PrimaryIp1 primaryIp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.CreatePrimaryIpResponse;
import cloud.hetzner.api.models.Datacenter2;
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.PrimaryIp1;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.Status;
import cloud.hetzner.api.models.Type50;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

CreatePrimaryIpResponse createPrimaryIpResponse = new CreatePrimaryIpResponse.Builder(
    new PrimaryIp1.Builder(
        17,
        "server",
        true,
        false,
        "2016-01-30T23:55:00+00:00",
        new Datacenter2.Builder(
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
        Arrays.asList(
            new DnsPtr.Builder(
                "server.example.com",
                "2001:db8::1"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        42,
        "131.232.99.1",
        new LinkedHashMap<String, String>() {{
            put("key0", "labels2");
            put("key1", "labels1");
        }},
        "my-resource",
        new Protection.Builder(
            false
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        Type50.IPV4
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.action(new Action.Builder(
        "command6",
        new Error.Builder(
            "code2",
            "message4"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "finished0",
        238,
        143.26D,
        Arrays.asList(
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "started8",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



