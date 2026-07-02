# Notebook Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGE

Contains metadata for notebook, including the notebook name, ID, workgroup, and time created.

*This model accepts additional fields of type array.*


# Class Name

`NotebookMetadata`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getNotebookId(): ?string | setNotebookId(?string notebookId): void |
| `name` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): ?string | setName(?string name): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `creationTime` | `?DateTime` | Optional | - | getCreationTime(): ?\DateTime | setCreationTime(?\DateTime creationTime): void |
| `type` | [`?string(NotebookType1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/notebook-type-1.md) | Optional | - | getType(): ?string | setType(?string type): void |
| `lastModifiedTime` | `?DateTime` | Optional | - | getLastModifiedTime(): ?\DateTime | setLastModifiedTime(?\DateTime lastModifiedTime): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\NotebookMetadataBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\NotebookType1;
use AmazonAthenaLib\ApiHelper;

$notebookMetadata = NotebookMetadataBuilder::init()
    ->notebookId('NotebookId0')
    ->name('Name0')
    ->workGroup('WorkGroup2')
    ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->type(NotebookType1::IPYNB)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



