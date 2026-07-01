# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/iso.md) | Required | - | getIso(): Iso | setIso(Iso iso): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\IsosResponse1Builder;
use HetznerCloudAPILib\Models\Builders\IsoBuilder;
use HetznerCloudAPILib\Models\Type26Enum;

$isosResponse1 = IsosResponse1Builder::init(
    IsoBuilder::init(
        'FreeBSD 11.0 x64',
        42,
        Type26Enum::PUBLIC_
    )
        ->deprecated('2018-02-28T00:00:00+00:00')
        ->name('FreeBSD-11.0-RELEASE-amd64-dvd1')
        ->build()
)->build();
```



