# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type array.*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `fingerprint` | `string` | Required | Fingerprint of public key | getFingerprint(): string | setFingerprint(string fingerprint): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `publicKey` | `string` | Required | Public key | getPublicKey(): string | setPublicKey(string publicKey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\SshKeyBuilder;
use HetznerCloudApiLib\ApiHelper;

$sshKey = SshKeyBuilder::init(
    '2016-01-30T23:55:00+00:00',
    'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
    42,
    [
        'key0' => 'labels4',
        'key1' => 'labels3',
        'key2' => 'labels2'
    ],
    'my-resource',
    'ssh-rsa AAAjjk76kgf...Xt'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



