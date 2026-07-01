# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ServerType` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-type.md) | Required | - | ServerType getServerType() | setServerType(ServerType serverType) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CpuType;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.ServerType;
import cloud.hetzner.api.models.ServerTypesResponse1;
import cloud.hetzner.api.models.StorageType;
import java.io.IOException;
import java.util.Arrays;

ServerTypesResponse1 serverTypesResponse1 = new ServerTypesResponse1.Builder(
    new ServerType.Builder(
        1D,
        CpuType.SHARED,
        false,
        "CX11",
        24D,
        1D,
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
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



