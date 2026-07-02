# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQuery` | [`?NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/named-query-1.md) | Optional | - | getNamedQuery(): ?NamedQuery1 | setNamedQuery(?NamedQuery1 namedQuery): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetNamedQueryOutputBuilder;
use AmazonAthenaLib\Models\Builders\NamedQuery1Builder;
use AmazonAthenaLib\ApiHelper;

$getNamedQueryOutput = GetNamedQueryOutputBuilder::init()
    ->namedQuery(
        NamedQuery1Builder::init(
            'Name0',
            'Database8',
            'QueryString2'
        )
            ->description('Description6')
            ->namedQueryId('NamedQueryId2')
            ->workGroup('WorkGroup2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



