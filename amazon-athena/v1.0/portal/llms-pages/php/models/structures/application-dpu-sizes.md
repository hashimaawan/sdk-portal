# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.

*This model accepts additional fields of type array.*


# Class Name

`ApplicationDpuSizes`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applicationRuntimeId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getApplicationRuntimeId(): ?string | setApplicationRuntimeId(?string applicationRuntimeId): void |
| `supportedDpuSizes` | `?(int[])` | Optional | - | getSupportedDpuSizes(): ?array | setSupportedDpuSizes(?array supportedDpuSizes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ApplicationDpuSizesBuilder;
use AmazonAthenaLib\ApiHelper;

$applicationDpuSizes = ApplicationDpuSizesBuilder::init()
    ->applicationRuntimeId('ApplicationRuntimeId4')
    ->supportedDpuSizes(
        [
            17,
            18
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



