# Get Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookMetadata` | [`?NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/notebook-metadata-1.md) | Optional | - | getNotebookMetadata(): ?NotebookMetadata1 | setNotebookMetadata(?NotebookMetadata1 notebookMetadata): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetNotebookMetadataOutputBuilder;
use AmazonAthenaLib\Models\Builders\NotebookMetadata1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\NotebookType1Enum;

$getNotebookMetadataOutput = GetNotebookMetadataOutputBuilder::init()
    ->notebookMetadata(
        NotebookMetadata1Builder::init()
            ->notebookId('NotebookId0')
            ->name('Name0')
            ->workGroup('WorkGroup2')
            ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->type(NotebookType1Enum::IPYNB)
            ->build()
    )
    ->build();
```



