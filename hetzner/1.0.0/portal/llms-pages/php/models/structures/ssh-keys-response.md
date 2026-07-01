# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `sshKeys` | [`SshKey[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ssh-key.md) | Required | - | getSshKeys(): array | setSshKeys(array sshKeys): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\SshKeysResponseBuilder;
use HetznerCloudApiLib\Models\Builders\SshKeyBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\MetaBuilder;
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;

$sshKeysResponse = SshKeysResponseBuilder::init(
    [
        SshKeyBuilder::init(
            '2016-01-30T23:55:00+00:00',
            'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
            42,
            [
                'key0' => 'labels4',
                'key1' => 'labels5',
                'key2' => 'labels6'
            ],
            'my-resource',
            'ssh-rsa AAAjjk76kgf...Xt'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->meta(
        MetaBuilder::init(
            PaginationBuilder::init(
                17.58,
                13.34
            )
                ->lastPage(77.7)
                ->nextPage(209.18)
                ->previousPage(50.02)
                ->totalEntries(206.64)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



