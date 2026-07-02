# List Notebook Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`ListNotebookSessionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getNotebookId(): string | setNotebookId(string notebookId): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 100` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListNotebookSessionsRequestBuilder;
use AmazonAthenaLib\ApiHelper;

$listNotebookSessionsRequest = ListNotebookSessionsRequestBuilder::init(
    'NotebookId8'
)
    ->maxResults(14)
    ->nextToken('NextToken8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



