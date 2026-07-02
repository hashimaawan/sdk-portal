# Update Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rSW5wdXQ


# Class Name

`UpdateNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getNotebookId(): string | setNotebookId(string notebookId): void |
| `payload` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | getPayload(): string | setPayload(string payload): void |
| `type` | [`string(NotebookType2Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/notebook-type-2.md) | Required | - | getType(): string | setType(string type): void |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UpdateNotebookInputBuilder;
use AmazonAthenaLib\Models\NotebookType2Enum;

$updateNotebookInput = UpdateNotebookInputBuilder::init(
    'NotebookId8',
    'Payload4',
    NotebookType2Enum::IPYNB
)
    ->sessionId('SessionId0')
    ->clientRequestToken('ClientRequestToken2')
    ->build();
```



