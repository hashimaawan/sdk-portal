# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | Name of the SSH key | getName(): string | setName(string name): void |
| `publicKey` | `string` | Required | Public key | getPublicKey(): string | setPublicKey(string publicKey): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\SshKeysRequestBuilder;
use HetznerCloudAPILib\ApiHelper;

$sshKeysRequest = SshKeysRequestBuilder::init(
    'My ssh key',
    'ssh-rsa AAAjjk76kgf...Xt'
)
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



