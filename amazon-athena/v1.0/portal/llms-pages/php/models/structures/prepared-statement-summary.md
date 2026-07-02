# Prepared Statement Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50U3VtbWFyeQ

The name and last modified time of the prepared statement.

*This model accepts additional fields of type array.*


# Class Name

`PreparedStatementSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `statementName` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | getStatementName(): ?string | setStatementName(?string statementName): void |
| `lastModifiedTime` | `?DateTime` | Optional | - | getLastModifiedTime(): ?\DateTime | setLastModifiedTime(?\DateTime lastModifiedTime): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\PreparedStatementSummaryBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\ApiHelper;

$preparedStatementSummary = PreparedStatementSummaryBuilder::init()
    ->statementName('StatementName4')
    ->lastModifiedTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



