# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0


# Class Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `preparedStatement` | [`?PreparedStatement1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/prepared-statement-1.md) | Optional | - | getPreparedStatement(): ?PreparedStatement1 | setPreparedStatement(?PreparedStatement1 preparedStatement): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetPreparedStatementOutputBuilder;
use AmazonAthenaLib\Models\Builders\PreparedStatement1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;

$getPreparedStatementOutput = GetPreparedStatementOutputBuilder::init()
    ->preparedStatement(
        PreparedStatement1Builder::init()
            ->statementName('StatementName4')
            ->queryStatement('QueryStatement8')
            ->workGroupName('WorkGroupName8')
            ->description('Description0')
            ->lastModifiedTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->build()
    )
    ->build();
```



