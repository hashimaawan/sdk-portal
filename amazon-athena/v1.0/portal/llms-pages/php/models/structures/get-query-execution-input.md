# Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uSW5wdXQ

*This model accepts additional fields of type array.*


# Class Name

`GetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): string | setQueryExecutionId(string queryExecutionId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetQueryExecutionInputBuilder;
use AmazonAthenaLib\ApiHelper;

$getQueryExecutionInput = GetQueryExecutionInputBuilder::init(
    'QueryExecutionId8'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



