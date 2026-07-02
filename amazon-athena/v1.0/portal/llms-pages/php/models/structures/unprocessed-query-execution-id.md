# Unprocessed Query Execution Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUXVlcnlFeGVjdXRpb25JZA

Describes a query execution that failed to process.

*This model accepts additional fields of type array.*


# Class Name

`UnprocessedQueryExecutionId`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): ?string | setQueryExecutionId(?string queryExecutionId): void |
| `errorCode` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getErrorCode(): ?string | setErrorCode(?string errorCode): void |
| `errorMessage` | `?string` | Optional | - | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UnprocessedQueryExecutionIdBuilder;
use AmazonAthenaLib\ApiHelper;

$unprocessedQueryExecutionId = UnprocessedQueryExecutionIdBuilder::init()
    ->queryExecutionId('QueryExecutionId6')
    ->errorCode('ErrorCode2')
    ->errorMessage('ErrorMessage8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



