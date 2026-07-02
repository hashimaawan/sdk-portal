# Update Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`UpdateDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getName(): string | setName(string name): void |
| `type` | [`string(DataCatalogType3Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/data-catalog-type-3.md) | Required | - | getType(): string | setType(string type): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `parameters` | [`?Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/parameters.md) | Optional | - | getParameters(): ?Parameters | setParameters(?Parameters parameters): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UpdateDataCatalogInputBuilder;
use AmazonAthenaLib\Models\DataCatalogType3Enum;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;

$updateDataCatalogInput = UpdateDataCatalogInputBuilder::init(
    'Name4',
    DataCatalogType3Enum::GLUE
)
    ->description('Description2')
    ->parameters(
        ParametersBuilder::init()->build()
    )->build();
```



