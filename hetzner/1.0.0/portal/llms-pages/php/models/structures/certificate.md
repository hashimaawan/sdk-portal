# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type array.*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificate` | `?string` | Required | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding | getCertificate(): ?string | setCertificate(?string certificate): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `domainNames` | `string[]` | Required | Domains and subdomains covered by the Certificate | getDomainNames(): array | setDomainNames(array domainNames): void |
| `fingerprint` | `?string` | Required | SHA256 fingerprint of the Certificate | getFingerprint(): ?string | setFingerprint(?string fingerprint): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `notValidAfter` | `?string` | Required | Point in time when the Certificate stops being valid (in ISO-8601 format) | getNotValidAfter(): ?string | setNotValidAfter(?string notValidAfter): void |
| `notValidBefore` | `?string` | Required | Point in time when the Certificate becomes valid (in ISO-8601 format) | getNotValidBefore(): ?string | setNotValidBefore(?string notValidBefore): void |
| `status` | [`?Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/status-2.md) | Optional | Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates | getStatus(): ?Status2 | setStatus(?Status2 status): void |
| `type` | [`?string(Type)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type.md) | Optional | Type of the Certificate | getType(): ?string | setType(?string type): void |
| `usedBy` | [`UsedBy[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/used-by.md) | Required | Resources currently using the Certificate | getUsedBy(): array | setUsedBy(array usedBy): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CertificateBuilder;
use HetznerCloudApiLib\Models\Builders\UsedByBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Status2Builder;
use HetznerCloudApiLib\Models\Issuance;
use HetznerCloudApiLib\Models\Renewal;
use HetznerCloudApiLib\Models\Type;

$certificate = CertificateBuilder::init(
    '2016-01-30T23:55:00+00:00',
    [
        'example.com',
        'webmail.example.com',
        'www.example.com'
    ],
    42,
    [
        'key0' => 'labels8',
        'key1' => 'labels7',
        'key2' => 'labels6'
    ],
    'my-resource',
    [
        UsedByBuilder::init(
            4711,
            'load_balancer'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->certificate('-----BEGIN CERTIFICATE-----
...')
    ->fingerprint('03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f')
    ->notValidAfter('2019-07-08T09:59:59+00:00')
    ->notValidBefore('2019-01-08T10:00:00+00:00')
    ->status(
        Status2Builder::init()
            ->error(
                null
            )
            ->issuance(Issuance::COMPLETED)
            ->renewal(Renewal::FAILED)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->type(Type::UPLOADED)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



