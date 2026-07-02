# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalogName(): ?string | setCatalogName(?string catalogName): void |
| `type` | [`?string(DataCatalogType2Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/data-catalog-type-2.md) | Optional | - | getType(): ?string | setType(?string type): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DataCatalogSummaryBuilder;
use AmazonAthenaLib\Models\DataCatalogType2Enum;

$dataCatalogSummary = DataCatalogSummaryBuilder::init()
    ->catalogName('CatalogName2')
    ->type(DataCatalogType2Enum::HIVE)
    ->build();
```



