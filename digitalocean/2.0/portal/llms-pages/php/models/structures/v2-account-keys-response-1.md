# V2 Account Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBY2NvdW50JTI1MjBLZXlzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AccountKeysResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sshKey` | [`?SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/ssh-key.md) | Optional | - | getSshKey(): ?SshKey | setSshKey(?SshKey sshKey): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AccountKeysResponse1Builder;
use DigitalOceanApiLib\Models\Builders\SshKeyBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AccountKeysResponse1 = V2AccountKeysResponse1Builder::init()
    ->sshKey(
        SshKeyBuilder::init(
            'name2',
            'public_key4'
        )
            ->fingerprint('fingerprint8')
            ->id(204)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



