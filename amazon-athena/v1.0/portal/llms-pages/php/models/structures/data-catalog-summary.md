# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.

*This model accepts additional fields of type array.*


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalogName(): ?string | setCatalogName(?string catalogName): void |
| `type` | [`?string(DataCatalogType2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/data-catalog-type-2.md) | Optional | - | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DataCatalogSummaryBuilder;
use AmazonAthenaLib\Models\DataCatalogType2;
use AmazonAthenaLib\ApiHelper;

$dataCatalogSummary = DataCatalogSummaryBuilder::init()
    ->catalogName('CatalogName2')
    ->type(DataCatalogType2::HIVE)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



