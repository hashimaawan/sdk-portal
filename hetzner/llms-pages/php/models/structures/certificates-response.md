# Certificates Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlc1Jlc3BvbnNl


# Class Name

`CertificatesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificates` | [`Certificate[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/certificate.md) | Required | - | getCertificates(): array | setCertificates(array certificates): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CertificatesResponseBuilder;
use HetznerCloudAPILib\Models\Builders\CertificateBuilder;
use HetznerCloudAPILib\Models\Builders\UsedByBuilder;
use HetznerCloudAPILib\Models\Builders\Status2Builder;
use HetznerCloudAPILib\Models\IssuanceEnum;
use HetznerCloudAPILib\Models\RenewalEnum;
use HetznerCloudAPILib\Models\TypeEnum;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

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
                )->build()
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
                    ->issuance(IssuanceEnum::COMPLETED)
                    ->renewal(RenewalEnum::FAILED)
                    ->build()
            )
            ->type(TypeEnum::UPLOADED)
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
                ->build()
        )->build()
    )->build();
```



