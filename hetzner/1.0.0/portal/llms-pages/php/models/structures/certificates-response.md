# Certificates Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlc1Jlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`CertificatesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificates` | [`Certificate[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/certificate.md) | Required | - | getCertificates(): array | setCertificates(array certificates): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CertificatesResponseBuilder;
use HetznerCloudApiLib\Models\Builders\CertificateBuilder;
use HetznerCloudApiLib\Models\Builders\UsedByBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Status2Builder;
use HetznerCloudApiLib\Models\Issuance;
use HetznerCloudApiLib\Models\Renewal;
use HetznerCloudApiLib\Models\Type;
use HetznerCloudApiLib\Models\Builders\MetaBuilder;
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;

$certificatesResponse = CertificatesResponseBuilder::init(
    [
        CertificateBuilder::init(
            '2016-01-30T23:55:00+00:00',
            [
                'example.com',
                'webmail.example.com',
                'www.example.com'
            ],
            42,
            [
                'key0' => 'labels2',
                'key1' => 'labels1',
                'key2' => 'labels0'
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
            ->build()
    ]
)
    ->meta(
        MetaBuilder::init(
            PaginationBuilder::init(
                17.58,
                13.34
            )
                ->lastPage(77.7)
                ->nextPage(209.18)
                ->previousPage(50.02)
                ->totalEntries(206.64)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



