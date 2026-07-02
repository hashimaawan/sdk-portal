# Backup Restore

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhY2t1cFJlc3RvcmU

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`BackupRestore`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backupCreatedAt` | `string \| undefined` | Optional | The timestamp of an existing database cluster backup in ISO8601 combined date and time format. The most recent backup will be used if excluded. |
| `databaseName` | `string` | Required | The name of an existing database cluster from which the backup will be restored. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { BackupRestore } from 'digitalocean-apilib';

const backupRestore: BackupRestore = {
  databaseName: 'backend',
  backupCreatedAt: '2019-01-31T19:25:22Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



