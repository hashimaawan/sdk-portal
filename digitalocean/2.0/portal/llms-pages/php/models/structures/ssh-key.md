# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `fingerprint` | `?string` | Optional, Read-only | A unique identifier that differentiates this key from other keys using  a format that SSH recognizes. The fingerprint is created when the key is added to your account. | getFingerprint(): ?string | setFingerprint(?string fingerprint): void |
| `id` | `?int` | Optional, Read-only | A unique identification number for this key. Can be used to embed a  specific SSH key into a Droplet. | getId(): ?int | setId(?int id): void |
| `name` | `string` | Required | A human-readable display name for this key, used to easily identify the SSH keys when they are displayed. | getName(): string | setName(string name): void |
| `publicKey` | `string` | Required | The entire public key string that was uploaded. Embedded into the root user's `authorized_keys` file if you include this key during Droplet creation. | getPublicKey(): string | setPublicKey(string publicKey): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\SshKeyBuilder;
use DigitalOceanApiLib\ApiHelper;

$sshKey = SshKeyBuilder::init(
    'My SSH Public Key',
    'ssh-rsa AEXAMPLEaC1yc2EAAAADAQABAAAAQQDDHr/jh2Jy4yALcK4JyWbVkPRaWmhck3IgCoeOO3z1e2dBowLh64QAM+Qb72pxekALga2oi4GvT+TlWNhzPH4V example'
)
    ->fingerprint('3b:16:bf:e4:8b:00:8b:b8:59:8c:a9:d3:f0:19:45:fa')
    ->id(512189)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



