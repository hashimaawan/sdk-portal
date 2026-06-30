# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `error` | [`?Error2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened | getError(): ?Error2 | setError(?Error2 error): void |
| `issuance` | [`?string(IssuanceEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate | getIssuance(): ?string | setIssuance(?string issuance): void |
| `renewal` | [`?string(RenewalEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. | getRenewal(): ?string | setRenewal(?string renewal): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Status2Builder;
use HetznerCloudAPILib\Models\IssuanceEnum;
use HetznerCloudAPILib\Models\RenewalEnum;

$status2 = Status2Builder::init()
    ->error(
        null
    )
    ->issuance(IssuanceEnum::COMPLETED)
    ->renewal(RenewalEnum::SCHEDULED)
    ->build();
```



