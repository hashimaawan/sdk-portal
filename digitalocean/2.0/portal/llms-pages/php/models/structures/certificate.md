# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the certificate was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `dnsNames` | `?(string[])` | Optional | An array of fully qualified domain names (FQDNs) for which the certificate was issued. | getDnsNames(): ?array | setDnsNames(?array dnsNames): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a certificate. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | A unique human-readable name referring to a certificate. | getName(): ?string | setName(?string name): void |
| `notAfter` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents the certificate's expiration date. | getNotAfter(): ?\DateTime | setNotAfter(?\DateTime notAfter): void |
| `sha1Fingerprint` | `?string` | Optional, Read-only | A unique identifier generated from the SHA-1 fingerprint of the certificate. | getSha1Fingerprint(): ?string | setSha1Fingerprint(?string sha1Fingerprint): void |
| `state` | [`?string(State)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/state.md) | Optional, Read-only | A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`. | getState(): ?string | setState(?string state): void |
| `type` | [`?string(Type4)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\CertificateBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\State;
use DigitalOceanApiLib\Models\Type4;
use DigitalOceanApiLib\ApiHelper;

$certificate = CertificateBuilder::init()
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2017-02-08T16:02:37Z'))
    ->dnsNames(
        [
            'www.example.com',
            'example.com'
        ]
    )
    ->id('892071a0-bb95-49bc-8021-3afd67a210bf')
    ->name('web-cert-01')
    ->notAfter(DateTimeHelper::fromRfc3339DateTime('2017-02-22T00:23:00Z'))
    ->sha1Fingerprint('dfcc9f57d86bf58e321c2c6c31c7a971be244ac7')
    ->state(State::VERIFIED)
    ->type(Type4::LETS_ENCRYPT)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



