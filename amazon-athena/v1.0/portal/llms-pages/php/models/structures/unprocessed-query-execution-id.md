# Unprocessed Query Execution Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUXVlcnlFeGVjdXRpb25JZA

Describes a query execution that failed to process.


# Class Name

`UnprocessedQueryExecutionId`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): ?string | setQueryExecutionId(?string queryExecutionId): void |
| `errorCode` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getErrorCode(): ?string | setErrorCode(?string errorCode): void |
| `errorMessage` | `?string` | Optional | - | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UnprocessedQueryExecutionIdBuilder;

$unprocessedQueryExecutionId = UnprocessedQueryExecutionIdBuilder::init()
    ->queryExecutionId('QueryExecutionId6')
    ->errorCode('ErrorCode2')
    ->errorMessage('ErrorMessage8')
    ->build();
```



