# Let S Encrypt Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkxldCUyNTI3cyUyNTIwRW5jcnlwdCUyNTIwQ2VydGlmaWNhdGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`LetSEncryptCertificateRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | A unique human-readable name referring to a certificate. | getName(): string | setName(string name): void |
| `type` | [`?string(Type4)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. | getType(): ?string | setType(?string type): void |
| `dnsNames` | `string[]` | Required | An array of fully qualified domain names (FQDNs) for which the certificate was issued. A certificate covering all subdomains can be issued using a wildcard (e.g. `*.example.com`). | getDnsNames(): array | setDnsNames(array dnsNames): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\LetSEncryptCertificateRequestBuilder;
use DigitalOceanApiLib\Models\Type4;
use DigitalOceanApiLib\ApiHelper;

$letSEncryptCertificateRequest = LetSEncryptCertificateRequestBuilder::init(
    'web-cert-01',
    [
        'www.example.com',
        'example.com'
    ]
)
    ->type(Type4::LETS_ENCRYPT)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



