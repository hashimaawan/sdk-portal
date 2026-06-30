# Server Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlclR5cGU


# Class Name

`ServerType`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cores` | `double` | Required | Number of cpu cores a Server of this type will have | double getCores() | setCores(double cores) |
| `CpuType` | [`CpuTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/cpu-type.md) | Required | Type of cpu | CpuTypeEnum getCpuType() | setCpuType(CpuTypeEnum cpuType) |
| `Deprecated` | `boolean` | Required | True if Server type is deprecated | boolean getDeprecated() | setDeprecated(boolean deprecated) |
| `Description` | `String` | Required | Description of the Server type | String getDescription() | setDescription(String description) |
| `Disk` | `double` | Required | Disk size a Server of this type will have in GB | double getDisk() | setDisk(double disk) |
| `Id` | `double` | Required | ID of the Server type | double getId() | setId(double id) |
| `Memory` | `double` | Required | Memory a Server of this type will have in GB | double getMemory() | setMemory(double memory) |
| `Name` | `String` | Required | Unique identifier of the Server type | String getName() | setName(String name) |
| `Prices` | [`List<Price9>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/price-9.md) | Required | Prices in different Locations | List<Price9> getPrices() | setPrices(List<Price9> prices) |
| `StorageType` | [`StorageTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. | StorageTypeEnum getStorageType() | setStorageType(StorageTypeEnum storageType) |


# Example

```java
import cloud.hetzner.api.models.CpuTypeEnum;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.ServerType;
import cloud.hetzner.api.models.StorageTypeEnum;
import java.util.Arrays;

ServerType serverType = new ServerType.Builder(
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
.build();
```



