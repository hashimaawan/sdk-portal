# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ

*This model accepts additional fields of type array.*


# Class Name

`ListApplicationDpuSizesInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 100` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListApplicationDpuSizesInputBuilder;
use AmazonAthenaLib\ApiHelper;

$listApplicationDpuSizesInput = ListApplicationDpuSizesInputBuilder::init()
    ->maxResults(56)
    ->nextToken('NextToken6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



