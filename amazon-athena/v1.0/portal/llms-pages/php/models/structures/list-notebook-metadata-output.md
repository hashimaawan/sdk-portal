# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0


# Class Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `notebookMetadataList` | [`?(NotebookMetadata[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/notebook-metadata.md) | Optional | - | getNotebookMetadataList(): ?array | setNotebookMetadataList(?array notebookMetadataList): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListNotebookMetadataOutputBuilder;
use AmazonAthenaLib\Models\Builders\NotebookMetadataBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\NotebookType1Enum;

$listNotebookMetadataOutput = ListNotebookMetadataOutputBuilder::init()
    ->nextToken('NextToken2')
    ->notebookMetadataList(
        [
            NotebookMetadataBuilder::init()
                ->notebookId('NotebookId4')
                ->name('Name4')
                ->workGroup('WorkGroup6')
                ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->type(NotebookType1Enum::IPYNB)
                ->build()
        ]
    )
    ->build();
```



