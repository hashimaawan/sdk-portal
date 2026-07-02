# List Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhSW5wdXQ


# Class Name

`ListNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `filters` | [`?Filters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/filters.md) | Optional | - | getFilters(): ?Filters | setFilters(?Filters filters): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListNotebookMetadataInputBuilder;
use AmazonAthenaLib\Models\Builders\FiltersBuilder;

$listNotebookMetadataInput = ListNotebookMetadataInputBuilder::init(
    'WorkGroup4'
)
    ->filters(
        FiltersBuilder::init()
            ->name('Name2')
            ->build()
    )
    ->nextToken('NextToken2')
    ->maxResults(50)
    ->build();
```



