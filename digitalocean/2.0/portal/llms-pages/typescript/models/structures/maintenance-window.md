# Maintenance Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlV2luZG93

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`MaintenanceWindow`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `day` | `string` | Required | The day of the week on which to apply maintenance updates. |
| `description` | `string[] \| undefined` | Optional, Read-only | A list of strings, each containing information about a pending maintenance update. |
| `hour` | `string` | Required | The hour in UTC at which maintenance updates will be applied in 24 hour format. |
| `pending` | `boolean \| undefined` | Optional, Read-only | A boolean value indicating whether any maintenance is scheduled to be performed in the next window. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { MaintenanceWindow } from 'digitalocean-apilib';

const maintenanceWindow: MaintenanceWindow = {
  day: 'tuesday',
  hour: '14:00',
  description: [
    'Update TimescaleDB to version 1.2.1',
    'Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases'
  ],
  pending: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



