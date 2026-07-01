# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.

*This model accepts additional fields of type array.*


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `count` | `?int` | Optional | Total number of items returned. | getCount(): ?int | setCount(?int count): void |
| `offset` | `?int` | Optional | Position in pagination. | getOffset(): ?int | setOffset(?int offset): void |
| `totalCount` | `?int` | Optional | Total number of items available. | getTotalCount(): ?int | setTotalCount(?int totalCount): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use GiphyApiLib\Models\Builders\PaginationBuilder;
use GiphyApiLib\ApiHelper;

$pagination = PaginationBuilder::init()
    ->count(25)
    ->offset(75)
    ->totalCount(250)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



