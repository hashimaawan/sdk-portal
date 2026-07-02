# Unprocessed Prepared Statement Name

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUHJlcGFyZWRTdGF0ZW1lbnROYW1l

The name of a prepared statement that could not be returned.


# Class Name

`UnprocessedPreparedStatementName`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `statementName` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | getStatementName(): ?string | setStatementName(?string statementName): void |
| `errorCode` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getErrorCode(): ?string | setErrorCode(?string errorCode): void |
| `errorMessage` | `?string` | Optional | - | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UnprocessedPreparedStatementNameBuilder;

$unprocessedPreparedStatementName = UnprocessedPreparedStatementNameBuilder::init()
    ->statementName('StatementName8')
    ->errorCode('ErrorCode6')
    ->errorMessage('ErrorMessage6')
    ->build();
```



