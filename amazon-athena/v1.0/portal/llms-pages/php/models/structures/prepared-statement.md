# Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50

A prepared SQL statement for use with Athena.

*This model accepts additional fields of type array.*


# Class Name

`PreparedStatement`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `statementName` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | getStatementName(): ?string | setStatementName(?string statementName): void |
| `queryStatement` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | getQueryStatement(): ?string | setQueryStatement(?string queryStatement): void |
| `workGroupName` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroupName(): ?string | setWorkGroupName(?string workGroupName): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `lastModifiedTime` | `?DateTime` | Optional | - | getLastModifiedTime(): ?\DateTime | setLastModifiedTime(?\DateTime lastModifiedTime): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\PreparedStatementBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\ApiHelper;

$preparedStatement = PreparedStatementBuilder::init()
    ->statementName('StatementName8')
    ->queryStatement('QueryStatement2')
    ->workGroupName('WorkGroupName2')
    ->description('Description4')
    ->lastModifiedTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



