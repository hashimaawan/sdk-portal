# List Engine Versions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc0lucHV0

*This model accepts additional fields of type array.*


# Class Name

`ListEngineVersionsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 10` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListEngineVersionsInputBuilder;
use AmazonAthenaLib\ApiHelper;

$listEngineVersionsInput = ListEngineVersionsInputBuilder::init()
    ->nextToken('NextToken6')
    ->maxResults(10)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



