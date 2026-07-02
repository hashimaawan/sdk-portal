# V2 Account Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBY2NvdW50JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AccountResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `account` | [`?Account`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/account.md) | Optional | - | getAccount(): ?Account | setAccount(?Account account): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AccountResponseBuilder;
use DigitalOceanApiLib\Models\Builders\AccountBuilder;
use DigitalOceanApiLib\Models\Status;
use DigitalOceanApiLib\Models\Builders\TeamBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AccountResponse = V2AccountResponseBuilder::init()
    ->account(
        AccountBuilder::init(
            248,
            'email6',
            false,
            164,
            Status::WARNING,
            'status_message8',
            'uuid6'
        )
            ->team(
                TeamBuilder::init()
                    ->name('name0')
                    ->uuid('uuid6')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



