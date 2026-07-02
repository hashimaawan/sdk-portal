# Query Runtime Statistics Rows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NSb3dz

Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query.

*This model accepts additional fields of type array.*


# Class Name

`QueryRuntimeStatisticsRows`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `inputRows` | `?int` | Optional | - | getInputRows(): ?int | setInputRows(?int inputRows): void |
| `inputBytes` | `?int` | Optional | - | getInputBytes(): ?int | setInputBytes(?int inputBytes): void |
| `outputBytes` | `?int` | Optional | - | getOutputBytes(): ?int | setOutputBytes(?int outputBytes): void |
| `outputRows` | `?int` | Optional | - | getOutputRows(): ?int | setOutputRows(?int outputRows): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatisticsRowsBuilder;
use AmazonAthenaLib\ApiHelper;

$queryRuntimeStatisticsRows = QueryRuntimeStatisticsRowsBuilder::init()
    ->inputRows(234)
    ->inputBytes(254)
    ->outputBytes(40)
    ->outputRows(226)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



