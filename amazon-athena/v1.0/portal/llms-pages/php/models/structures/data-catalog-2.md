# Data Catalog 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nMg

*This model accepts additional fields of type array.*


# Class Name

`DataCatalog2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getName(): string | setName(string name): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `type` | [`string(DataCatalogType1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/data-catalog-type-1.md) | Required | - | getType(): string | setType(string type): void |
| `parameters` | [`?Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/parameters.md) | Optional | - | getParameters(): ?Parameters | setParameters(?Parameters parameters): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DataCatalog2Builder;
use AmazonAthenaLib\Models\DataCatalogType1;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;
use AmazonAthenaLib\ApiHelper;

$dataCatalog2 = DataCatalog2Builder::init(
    'Name6',
    DataCatalogType1::LAMBDA
)
    ->description('Description0')
    ->parameters(
        ParametersBuilder::init()
            ->additionalProperty('exampleAdditionalProperty', 'Parameters_additionalProperties2')
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



