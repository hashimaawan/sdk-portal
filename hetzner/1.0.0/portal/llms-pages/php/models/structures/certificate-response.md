# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/certificate.md) | Required | - | getCertificate(): Certificate | setCertificate(Certificate certificate): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CertificateResponseBuilder;
use HetznerCloudApiLib\Models\Builders\CertificateBuilder;
use HetznerCloudApiLib\Models\Builders\UsedByBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Status2Builder;
use HetznerCloudApiLib\Models\Issuance;
use HetznerCloudApiLib\Models\Renewal;
use HetznerCloudApiLib\Models\Type;

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
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



