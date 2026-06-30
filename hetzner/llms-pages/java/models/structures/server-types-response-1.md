# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ServerType` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/server-type.md) | Required | - | ServerType getServerType() | setServerType(ServerType serverType) |


# Example

```java
import cloud.hetzner.api.models.CpuTypeEnum;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.ServerType;
import cloud.hetzner.api.models.ServerTypesResponse1;
import cloud.hetzner.api.models.StorageTypeEnum;
import java.util.Arrays;

ServerTypesResponse1 serverTypesResponse1 = new ServerTypesResponse1.Builder(
    new ServerType.Builder(
        1D,
        CpuTypeEnum.SHARED,
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
                .build(),
                new PriceMonthly10.Builder(
                    "1.1900000000000000",
                    "1.0000000000"
                )
                .build()
            )
            .build()
        ),
        StorageTypeEnum.LOCAL
    )
    .build()
)
.build();
```



