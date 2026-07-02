# Status 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXR1czEx

An object containing a `state` attribute whose value is set to a string indicating the current status of the cluster.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Status11`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `message` | `?string` | Optional | An optional message providing additional information about the current cluster state. | getMessage(): ?string | setMessage(?string message): void |
| `state` | [`?string(State2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/state-2.md) | Optional | A string indicating the current status of the cluster. | getState(): ?string | setState(?string state): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Status11Builder;
use DigitalOceanApiLib\Models\State2;
use DigitalOceanApiLib\ApiHelper;

$status11 = Status11Builder::init()
    ->message('provisioning')
    ->state(State2::PROVISIONING)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



