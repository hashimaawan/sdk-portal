# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

*This model accepts additional fields of type array.*


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `lastPage` | `?float` | Required | ID of the last page available. Can be null if the current page is the last one. | getLastPage(): ?float | setLastPage(?float lastPage): void |
| `nextPage` | `?float` | Required | ID of the next page. Can be null if the current page is the last one. | getNextPage(): ?float | setNextPage(?float nextPage): void |
| `page` | `float` | Required | Current page number | getPage(): float | setPage(float page): void |
| `perPage` | `float` | Required | Maximum number of items shown per page in the response | getPerPage(): float | setPerPage(float perPage): void |
| `previousPage` | `?float` | Required | ID of the previous page. Can be null if the current page is the first one. | getPreviousPage(): ?float | setPreviousPage(?float previousPage): void |
| `totalEntries` | `?float` | Required | The total number of entries that exist in the database for this query. Nullable if unknown. | getTotalEntries(): ?float | setTotalEntries(?float totalEntries): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;
use HetznerCloudApiLib\ApiHelper;

$pagination = PaginationBuilder::init(
    3,
    25
)
    ->lastPage(4)
    ->nextPage(4)
    ->previousPage(2)
    ->totalEntries(100)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



