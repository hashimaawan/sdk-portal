# Create Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CreateCertificateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/nullable-action.md) | Optional | - | getAction(): ?NullableAction | setAction(?NullableAction action): void |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/certificate.md) | Required | - | getCertificate(): Certificate | setCertificate(Certificate certificate): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreateCertificateResponseBuilder;
use HetznerCloudAPILib\Models\Builders\CertificateBuilder;
use HetznerCloudAPILib\Models\Builders\UsedByBuilder;
use HetznerCloudAPILib\Models\Builders\Status2Builder;
use HetznerCloudAPILib\Models\IssuanceEnum;
use HetznerCloudAPILib\Models\RenewalEnum;
use HetznerCloudAPILib\Models\TypeEnum;
use HetznerCloudAPILib\Models\Builders\NullableActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$createCertificateResponse = CreateCertificateResponseBuilder::init(
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
)
    ->action(
        NullableActionBuilder::init(
            'command6',
            238,
            143.26,
            [
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build()
            ],
            'started8',
            StatusEnum::RUNNING
        )
            ->error(
                ErrorBuilder::init(
                    'code2',
                    'message4'
                )->build()
            )
            ->finished('finished0')
            ->build()
    )
    ->build();
```



