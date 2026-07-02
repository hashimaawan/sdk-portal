# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dataCatalogsSummary` | [`?(DataCatalogSummary[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/data-catalog-summary.md) | Optional | - | getDataCatalogsSummary(): ?array | setDataCatalogsSummary(?array dataCatalogsSummary): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListDataCatalogsOutputBuilder;
use AmazonAthenaLib\Models\Builders\DataCatalogSummaryBuilder;
use AmazonAthenaLib\Models\DataCatalogType2;
use AmazonAthenaLib\ApiHelper;

$listDataCatalogsOutput = ListDataCatalogsOutputBuilder::init()
    ->dataCatalogsSummary(
        [
            DataCatalogSummaryBuilder::init()
                ->catalogName('CatalogName4')
                ->type(DataCatalogType2::HIVE)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DataCatalogSummaryBuilder::init()
                ->catalogName('CatalogName4')
                ->type(DataCatalogType2::HIVE)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DataCatalogSummaryBuilder::init()
                ->catalogName('CatalogName4')
                ->type(DataCatalogType2::HIVE)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->nextToken('NextToken0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



