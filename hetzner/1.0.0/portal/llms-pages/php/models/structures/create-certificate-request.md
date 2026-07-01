# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`CreateCertificateRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificate` | `?string` | Optional | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding. Required for type `uploaded` Certificates. | getCertificate(): ?string | setCertificate(?string certificate): void |
| `domainNames` | `?(string[])` | Optional | Domains and subdomains that should be contained in the Certificate issued by *Let's Encrypt*. Required for type `managed` Certificates. | getDomainNames(): ?array | setDomainNames(?array domainNames): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | Name of the Certificate | getName(): string | setName(string name): void |
| `privateKey` | `?string` | Optional | Certificate key in PEM format. Required for type `uploaded` Certificates. | getPrivateKey(): ?string | setPrivateKey(?string privateKey): void |
| `type` | [`?string(Type1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateCertificateRequestBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Type1;

$createCertificateRequest = CreateCertificateRequestBuilder::init(
    'my website cert'
)
    ->certificate('-----BEGIN CERTIFICATE-----
...')
    ->domainNames(
        [
            'domain_names8',
            'domain_names9',
            'domain_names0'
        ]
    )
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->privateKey('-----BEGIN PRIVATE KEY-----
...')
    ->type(Type1::UPLOADED)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



