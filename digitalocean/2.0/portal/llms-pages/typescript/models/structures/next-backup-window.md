# Next Backup Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk5leHRCYWNrdXBXaW5kb3c

The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`NextBackupWindow`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `end` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format specifying the end of the Droplet's backup window. |
| `start` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format specifying the start of the Droplet's backup window. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { NextBackupWindow } from 'digitalocean-apilib';

const nextBackupWindow: NextBackupWindow = {
  end: '2019-12-04T23:00:00Z',
  start: '2019-12-04T00:00:00Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



