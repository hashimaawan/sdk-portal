# List Notebook Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`ListNotebookSessionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookSessionsList` | [`NotebookSessionSummary[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/notebook-session-summary.md) | Required | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` | getNotebookSessionsList(): array | setNotebookSessionsList(array notebookSessionsList): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListNotebookSessionsResponseBuilder;
use AmazonAthenaLib\Models\Builders\NotebookSessionSummaryBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\ApiHelper;

$listNotebookSessionsResponse = ListNotebookSessionsResponseBuilder::init(
    [
        NotebookSessionSummaryBuilder::init()
            ->sessionId('SessionId4')
            ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->nextToken('NextToken0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



