# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U


# Class Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `sshKeys` | [`SshKey[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/ssh-key.md) | Required | - | getSshKeys(): array | setSshKeys(array sshKeys): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\SshKeysResponseBuilder;
use HetznerCloudAPILib\Models\Builders\SshKeyBuilder;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

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
        )->build()
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
                ->build()
        )->build()
    )->build();
```



