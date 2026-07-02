# Start Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`StartQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): ?string | setQueryExecutionId(?string queryExecutionId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartQueryExecutionOutputBuilder;
use AmazonAthenaLib\ApiHelper;

$startQueryExecutionOutput = StartQueryExecutionOutputBuilder::init()
    ->queryExecutionId('QueryExecutionId0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



