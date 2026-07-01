# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `count` | `?int` | Optional | Total number of items returned. | getCount(): ?int | setCount(?int count): void |
| `offset` | `?int` | Optional | Position in pagination. | getOffset(): ?int | setOffset(?int offset): void |
| `totalCount` | `?int` | Optional | Total number of items available. | getTotalCount(): ?int | setTotalCount(?int totalCount): void |


# Example

```php
use GiphyAPILib\Models\Builders\PaginationBuilder;

$pagination = PaginationBuilder::init()
    ->count(25)
    ->offset(75)
    ->totalCount(250)
    ->build();
```



