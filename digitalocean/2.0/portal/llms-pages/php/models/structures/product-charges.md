# Product Charges

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlByb2R1Y3RDaGFyZ2Vz

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ProductCharges`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `?string` | Optional | Total amount charged | getAmount(): ?string | setAmount(?string amount): void |
| `items` | [`?(Item[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/item.md) | Optional | List of amount, and grouped aggregates by resource type. | getItems(): ?array | setItems(?array items): void |
| `name` | `?string` | Optional | Description of usage charges | getName(): ?string | setName(?string name): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ProductChargesBuilder;
use DigitalOceanApiLib\Models\Builders\ItemBuilder;
use DigitalOceanApiLib\ApiHelper;

$productCharges = ProductChargesBuilder::init()
    ->amount('12.34')
    ->items(
        [
            ItemBuilder::init()
                ->amount('10.00')
                ->count('1')
                ->name('Spaces Subscription')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ItemBuilder::init()
                ->amount('2.34')
                ->count('1')
                ->name('Database Clusters')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->name('Product usage charges')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



