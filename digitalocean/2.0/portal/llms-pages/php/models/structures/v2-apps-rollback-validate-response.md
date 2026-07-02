# V2 Apps Rollback Validate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwVmFsaWRhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsRollbackValidateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `error` | [`?Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/error.md) | Optional | - | getError(): ?Error | setError(?Error error): void |
| `valid` | `?bool` | Optional | Indicates whether the app can be rolled back to the specified deployment. | getValid(): ?bool | setValid(?bool valid): void |
| `warnings` | [`?(Warning[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/warning.md) | Optional | Contains a list of warnings that may cause the rollback to run under unideal circumstances. | getWarnings(): ?array | setWarnings(?array warnings): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsRollbackValidateResponseBuilder;
use DigitalOceanApiLib\Models\Builders\ErrorBuilder;
use DigitalOceanApiLib\Models\Code;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\WarningBuilder;

$v2AppsRollbackValidateResponse = V2AppsRollbackValidateResponseBuilder::init()
    ->error(
        ErrorBuilder::init()
            ->code(Code::INCOMPATIBLE_PHASE)
            ->components(
                [
                    'components3'
                ]
            )
            ->message('message4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->valid(false)
    ->warnings(
        [
            WarningBuilder::init()
                ->code(Code::EXCEEDED_REVISION_LIMIT)
                ->components(
                    [
                        'components3'
                    ]
                )
                ->message('message4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            WarningBuilder::init()
                ->code(Code::EXCEEDED_REVISION_LIMIT)
                ->components(
                    [
                        'components3'
                    ]
                )
                ->message('message4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



