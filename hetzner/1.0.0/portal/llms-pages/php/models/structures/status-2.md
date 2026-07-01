# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates

*This model accepts additional fields of type array.*


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `error` | [`?Error2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened | getError(): ?Error2 | setError(?Error2 error): void |
| `issuance` | [`?string(Issuance)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate | getIssuance(): ?string | setIssuance(?string issuance): void |
| `renewal` | [`?string(Renewal)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. | getRenewal(): ?string | setRenewal(?string renewal): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Status2Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Issuance;
use HetznerCloudApiLib\Models\Renewal;

$status2 = Status2Builder::init()
    ->error(
        null
    )
    ->issuance(Issuance::COMPLETED)
    ->renewal(Renewal::SCHEDULED)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



