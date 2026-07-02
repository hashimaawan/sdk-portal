# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ


# Class Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): string | setName(string name): void |
| `payload` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | getPayload(): string | setPayload(string payload): void |
| `type` | [`string(NotebookType2Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/notebook-type-2.md) | Required | - | getType(): string | setType(string type): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ImportNotebookInputBuilder;
use AmazonAthenaLib\Models\NotebookType2Enum;

$importNotebookInput = ImportNotebookInputBuilder::init(
    'WorkGroup2',
    'Name0',
    'Payload6',
    NotebookType2Enum::IPYNB
)
    ->clientRequestToken('ClientRequestToken4')
    ->build();
```



