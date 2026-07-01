# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type array.*


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/iso.md) | Required | - | getIso(): Iso | setIso(Iso iso): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\IsosResponse1Builder;
use HetznerCloudApiLib\Models\Builders\IsoBuilder;
use HetznerCloudApiLib\Models\Type26;
use HetznerCloudApiLib\ApiHelper;

$isosResponse1 = IsosResponse1Builder::init(
    IsoBuilder::init(
        'FreeBSD 11.0 x64',
        42,
        Type26::PUBLIC_
    )
        ->deprecated('2018-02-28T00:00:00+00:00')
        ->name('FreeBSD-11.0-RELEASE-amd64-dvd1')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



