# Layout

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkxheW91dA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Layout`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `numNodes` | `?int` | Optional | - | getNumNodes(): ?int | setNumNodes(?int numNodes): void |
| `sizes` | `?(string[])` | Optional, Read-only | An array of objects containing the slugs available with various node counts | getSizes(): ?array | setSizes(?array sizes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\LayoutBuilder;
use DigitalOceanApiLib\ApiHelper;

$layout = LayoutBuilder::init()
    ->numNodes(1)
    ->sizes(
        [
            'db-s-1vcpu-1gb',
            'db-s-1vcpu-2gb'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



