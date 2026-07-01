# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/certificate.md) | Required | - | getCertificate(): Certificate | setCertificate(Certificate certificate): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CertificateResponseBuilder;
use HetznerCloudAPILib\Models\Builders\CertificateBuilder;
use HetznerCloudAPILib\Models\Builders\UsedByBuilder;
use HetznerCloudAPILib\Models\Builders\Status2Builder;
use HetznerCloudAPILib\Models\IssuanceEnum;
use HetznerCloudAPILib\Models\RenewalEnum;
use HetznerCloudAPILib\Models\TypeEnum;

$certificateResponse = CertificateResponseBuilder::init(
    CertificateBuilder::init(
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
)->build();
```



