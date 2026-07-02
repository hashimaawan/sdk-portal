# Batch Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`BatchGetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `preparedStatementNames` | `string[]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | getPreparedStatementNames(): array | setPreparedStatementNames(array preparedStatementNames): void |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\BatchGetPreparedStatementInputBuilder;
use AmazonAthenaLib\ApiHelper;

$batchGetPreparedStatementInput = BatchGetPreparedStatementInputBuilder::init(
    [
        'PreparedStatementNames8',
        'PreparedStatementNames9',
        'PreparedStatementNames0'
    ],
    'WorkGroup6'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



