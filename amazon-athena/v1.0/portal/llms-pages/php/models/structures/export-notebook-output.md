# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0

*This model accepts additional fields of type array.*


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookMetadata` | [`?NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/notebook-metadata-1.md) | Optional | - | getNotebookMetadata(): ?NotebookMetadata1 | setNotebookMetadata(?NotebookMetadata1 notebookMetadata): void |
| `payload` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | getPayload(): ?string | setPayload(?string payload): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ExportNotebookOutputBuilder;
use AmazonAthenaLib\Models\Builders\NotebookMetadata1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\NotebookType1;
use AmazonAthenaLib\ApiHelper;

$exportNotebookOutput = ExportNotebookOutputBuilder::init()
    ->notebookMetadata(
        NotebookMetadata1Builder::init()
            ->notebookId('NotebookId0')
            ->name('Name0')
            ->workGroup('WorkGroup2')
            ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->type(NotebookType1::IPYNB)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->payload('Payload2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



