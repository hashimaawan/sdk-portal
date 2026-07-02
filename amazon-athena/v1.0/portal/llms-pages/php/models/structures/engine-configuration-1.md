# Engine Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type array.*


# Class Name

`EngineConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `coordinatorDpuSize` | `?int` | Optional | **Constraints**: `>= 1`, `<= 1` | getCoordinatorDpuSize(): ?int | setCoordinatorDpuSize(?int coordinatorDpuSize): void |
| `maxConcurrentDpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` | getMaxConcurrentDpus(): int | setMaxConcurrentDpus(int maxConcurrentDpus): void |
| `defaultExecutorDpuSize` | `?int` | Optional | **Constraints**: `>= 1`, `<= 1` | getDefaultExecutorDpuSize(): ?int | setDefaultExecutorDpuSize(?int defaultExecutorDpuSize): void |
| `additionalConfigs` | [`?AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/additional-configs.md) | Optional | - | getAdditionalConfigs(): ?AdditionalConfigs | setAdditionalConfigs(?AdditionalConfigs additionalConfigs): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\EngineConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\AdditionalConfigsBuilder;
use AmazonAthenaLib\ApiHelper;

$engineConfiguration1 = EngineConfiguration1Builder::init(
    214
)
    ->coordinatorDpuSize(1)
    ->defaultExecutorDpuSize(1)
    ->additionalConfigs(
        AdditionalConfigsBuilder::init()
            ->additionalProperty('exampleAdditionalProperty', 'AdditionalConfigs_additionalProperties5')
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



