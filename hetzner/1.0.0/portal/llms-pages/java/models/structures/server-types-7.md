# Server Types 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzNw

*This model accepts additional fields of type Object.*


# Class Name

`ServerTypes7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cores` | `double` | Required | Number of cpu cores a Server of this type will have | double getCores() | setCores(double cores) |
| `CpuType` | [`CpuType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/cpu-type.md) | Required | Type of cpu | CpuType getCpuType() | setCpuType(CpuType cpuType) |
| `Deprecated` | `boolean` | Required | True if Server type is deprecated | boolean getDeprecated() | setDeprecated(boolean deprecated) |
| `Description` | `String` | Required | Description of the Server type | String getDescription() | setDescription(String description) |
| `Disk` | `double` | Required | Disk size a Server of this type will have in GB | double getDisk() | setDisk(double disk) |
| `Id` | `double` | Required | ID of the Server type | double getId() | setId(double id) |
| `Memory` | `double` | Required | Memory a Server of this type will have in GB | double getMemory() | setMemory(double memory) |
| `Name` | `String` | Required | Unique identifier of the Server type | String getName() | setName(String name) |
| `Prices` | [`List<Price9>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-9.md) | Required | Prices in different Locations | List<Price9> getPrices() | setPrices(List<Price9> prices) |
| `StorageType` | [`StorageType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. | StorageType getStorageType() | setStorageType(StorageType storageType) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CpuType;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.ServerTypes7;
import cloud.hetzner.api.models.StorageType;
import java.io.IOException;
import java.util.Arrays;

ServerTypes7 serverTypes7 = new ServerTypes7.Builder(
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
.build();
```



