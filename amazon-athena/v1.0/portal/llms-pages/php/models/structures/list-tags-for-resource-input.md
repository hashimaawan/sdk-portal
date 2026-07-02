# List Tags for Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`ListTagsForResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | getResourceArn(): string | setResourceArn(string resourceArn): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 75` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListTagsForResourceInputBuilder;
use AmazonAthenaLib\ApiHelper;

$listTagsForResourceInput = ListTagsForResourceInputBuilder::init(
    'ResourceARN0'
)
    ->nextToken('NextToken0')
    ->maxResults(76)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



