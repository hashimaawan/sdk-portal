# Notebook Metadata 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGEx


# Class Name

`NotebookMetadata1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getNotebookId(): ?string | setNotebookId(?string notebookId): void |
| `name` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): ?string | setName(?string name): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `creationTime` | `?DateTime` | Optional | - | getCreationTime(): ?\DateTime | setCreationTime(?\DateTime creationTime): void |
| `type` | [`?string(NotebookType1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/notebook-type-1.md) | Optional | - | getType(): ?string | setType(?string type): void |
| `lastModifiedTime` | `?DateTime` | Optional | - | getLastModifiedTime(): ?\DateTime | setLastModifiedTime(?\DateTime lastModifiedTime): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\NotebookMetadata1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\NotebookType1Enum;

$notebookMetadata1 = NotebookMetadata1Builder::init()
    ->notebookId('NotebookId2')
    ->name('Name2')
    ->workGroup('WorkGroup4')
    ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->type(NotebookType1Enum::IPYNB)
    ->build();
```



