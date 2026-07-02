# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0

*This model accepts additional fields of type array.*


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dataCatalog` | [`?DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/data-catalog-2.md) | Optional | - | getDataCatalog(): ?DataCatalog2 | setDataCatalog(?DataCatalog2 dataCatalog): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetDataCatalogOutputBuilder;
use AmazonAthenaLib\Models\Builders\DataCatalog2Builder;
use AmazonAthenaLib\Models\DataCatalogType1;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;
use AmazonAthenaLib\ApiHelper;

$getDataCatalogOutput = GetDataCatalogOutputBuilder::init()
    ->dataCatalog(
        DataCatalog2Builder::init(
            'Name4',
            DataCatalogType1::GLUE
        )
            ->description('Description2')
            ->parameters(
                ParametersBuilder::init()
                    ->additionalProperty('exampleAdditionalProperty', 'Parameters_additionalProperties2')
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



