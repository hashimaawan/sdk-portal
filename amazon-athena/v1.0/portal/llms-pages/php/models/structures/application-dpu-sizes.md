# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.


# Class Name

`ApplicationDPUSizes`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applicationRuntimeId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getApplicationRuntimeId(): ?string | setApplicationRuntimeId(?string applicationRuntimeId): void |
| `supportedDPUSizes` | `?(int[])` | Optional | - | getSupportedDPUSizes(): ?array | setSupportedDPUSizes(?array supportedDPUSizes): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ApplicationDPUSizesBuilder;

$applicationDPUSizes = ApplicationDPUSizesBuilder::init()
    ->applicationRuntimeId('ApplicationRuntimeId2')
    ->supportedDPUSizes(
        [
            57
        ]
    )
    ->build();
```



