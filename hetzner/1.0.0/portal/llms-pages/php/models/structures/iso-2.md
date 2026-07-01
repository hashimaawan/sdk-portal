# Iso 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRklzbzI

ISO Image that is attached to this Server. Null if no ISO is attached.


# Class Name

`Iso2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `deprecated` | `?string` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. | getDeprecated(): ?string | setDeprecated(?string deprecated): void |
| `description` | `string` | Required | Description of the ISO | getDescription(): string | setDescription(string description): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `name` | `?string` | Required | Unique identifier of the ISO. Only set for public ISOs | getName(): ?string | setName(?string name): void |
| `type` | [`string(Type26Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-26.md) | Required | Type of the ISO | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Iso2Builder;
use HetznerCloudAPILib\Models\Type26Enum;

$iso2 = Iso2Builder::init(
    'FreeBSD 11.0 x64',
    42,
    Type26Enum::PUBLIC_
)
    ->deprecated('2018-02-28T00:00:00+00:00')
    ->name('FreeBSD-11.0-RELEASE-amd64-dvd1')
    ->build();
```



