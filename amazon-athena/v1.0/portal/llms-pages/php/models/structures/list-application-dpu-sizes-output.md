# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0

*This model accepts additional fields of type array.*


# Class Name

`ListApplicationDpuSizesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applicationDpuSizes` | [`?(ApplicationDpuSizes[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/application-dpu-sizes.md) | Optional | - | getApplicationDpuSizes(): ?array | setApplicationDpuSizes(?array applicationDpuSizes): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListApplicationDpuSizesOutputBuilder;
use AmazonAthenaLib\Models\Builders\ApplicationDpuSizesBuilder;
use AmazonAthenaLib\ApiHelper;

$listApplicationDpuSizesOutput = ListApplicationDpuSizesOutputBuilder::init()
    ->applicationDpuSizes(
        [
            ApplicationDpuSizesBuilder::init()
                ->applicationRuntimeId('ApplicationRuntimeId0')
                ->supportedDpuSizes(
                    [
                        113,
                        114
                    ]
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ApplicationDpuSizesBuilder::init()
                ->applicationRuntimeId('ApplicationRuntimeId0')
                ->supportedDpuSizes(
                    [
                        113,
                        114
                    ]
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->nextToken('NextToken0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



