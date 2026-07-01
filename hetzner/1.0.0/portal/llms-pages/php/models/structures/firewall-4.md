# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxsNA

*This model accepts additional fields of type array.*


# Class Name

`Firewall4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firewall` | `?int` | Optional | ID of the Firewall | getFirewall(): ?int | setFirewall(?int firewall): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Firewall4Builder;
use HetznerCloudApiLib\ApiHelper;

$firewall4 = Firewall4Builder::init()
    ->firewall(176)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



