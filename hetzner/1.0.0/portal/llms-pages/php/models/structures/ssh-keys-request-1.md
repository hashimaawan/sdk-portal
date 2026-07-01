# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE


# Class Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New name Name to set | getName(): ?string | setName(?string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\SshKeysRequest1Builder;
use HetznerCloudAPILib\ApiHelper;

$sshKeysRequest1 = SshKeysRequest1Builder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('My ssh key')
    ->build();
```



