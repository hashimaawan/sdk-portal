# Contains All Domains for the App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNvbnRhaW5zJTI1MjBhbGwlMjUyMGRvbWFpbnMlMjUyMGZvciUyNTIwdGhlJTI1MjBhcHA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ContainsAllDomainsForTheApp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificateExpiresAt` | `?DateTime` | Optional, Read-only | - | getCertificateExpiresAt(): ?\DateTime | setCertificateExpiresAt(?\DateTime certificateExpiresAt): void |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `phase` | [`?string(Phase1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1::UNKNOWN` | getPhase(): ?string | setPhase(?string phase): void |
| `progress` | [`?Progress1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/progress-1.md) | Optional | - | getProgress(): ?Progress1 | setProgress(?Progress1 progress): void |
| `rotateValidationRecords` | `?bool` | Optional, Read-only | - | getRotateValidationRecords(): ?bool | setRotateValidationRecords(?bool rotateValidationRecords): void |
| `spec` | [`?Domain`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/domain.md) | Optional | - | getSpec(): ?Domain | setSpec(?Domain spec): void |
| `validations` | [`?(ListOfTxtValidationRecord[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/list-of-txt-validation-record.md) | Optional | - | getValidations(): ?array | setValidations(?array validations): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ContainsAllDomainsForTheAppBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Phase1;
use DigitalOceanApiLib\Models\Builders\Progress1Builder;
use DigitalOceanApiLib\ApiHelper;

$containsAllDomainsForTheApp = ContainsAllDomainsForTheAppBuilder::init()
    ->certificateExpiresAt(DateTimeHelper::fromRfc3339DateTime('2024-01-29T23:59:59Z'))
    ->id('4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf')
    ->phase(Phase1::ACTIVE)
    ->progress(
        Progress1Builder::init()
            ->steps(
                [
                    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'),
                    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'),
                    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->rotateValidationRecords(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



