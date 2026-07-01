# Ssh Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type array.*


# Class Name

`SshKeysResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sshKey` | [`SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ssh-key.md) | Required | - | getSshKey(): SshKey | setSshKey(SshKey sshKey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\SshKeysResponse1Builder;
use HetznerCloudApiLib\Models\Builders\SshKeyBuilder;
use HetznerCloudApiLib\ApiHelper;

$sshKeysResponse1 = SshKeysResponse1Builder::init(
    SshKeyBuilder::init(
        '2016-01-30T23:55:00+00:00',
        'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
        42,
        [
            'key0' => 'labels0'
        ],
        'my-resource',
        'ssh-rsa AAAjjk76kgf...Xt'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



