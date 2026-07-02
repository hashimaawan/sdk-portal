# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dataCatalog` | [`?DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/data-catalog-2.md) | Optional | - | getDataCatalog(): ?DataCatalog2 | setDataCatalog(?DataCatalog2 dataCatalog): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetDataCatalogOutputBuilder;
use AmazonAthenaLib\Models\Builders\DataCatalog2Builder;
use AmazonAthenaLib\Models\DataCatalogType1Enum;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;

$getDataCatalogOutput = GetDataCatalogOutputBuilder::init()
    ->dataCatalog(
        DataCatalog2Builder::init(
            'Name4',
            DataCatalogType1Enum::GLUE
        )
            ->description('Description2')
            ->parameters(
                ParametersBuilder::init()->build()
            )->build()
    )->build();
```



