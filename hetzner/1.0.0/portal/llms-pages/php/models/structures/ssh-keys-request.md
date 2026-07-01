# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | Name of the SSH key | getName(): string | setName(string name): void |
| `publicKey` | `string` | Required | Public key | getPublicKey(): string | setPublicKey(string publicKey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\SshKeysRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$sshKeysRequest = SshKeysRequestBuilder::init(
    'My ssh key',
    'ssh-rsa AAAjjk76kgf...Xt'
)
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



