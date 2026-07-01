# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ServerTypes` | [`List<ServerTypes7>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-types-7.md) | Required | - | List<ServerTypes7> getServerTypes() | setServerTypes(List<ServerTypes7> serverTypes) |


# Example

```java
import cloud.hetzner.api.models.CpuTypeEnum;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.ServerTypes7;
import cloud.hetzner.api.models.ServerTypesResponse;
import cloud.hetzner.api.models.StorageTypeEnum;
import java.util.Arrays;

ServerTypesResponse serverTypesResponse = new ServerTypesResponse.Builder(
    Arrays.asList(
        new ServerTypes7.Builder(
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
)
.build();
```



