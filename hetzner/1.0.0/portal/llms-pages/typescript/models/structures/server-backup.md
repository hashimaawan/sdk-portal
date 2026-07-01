# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage

*This model accepts additional fields of type unknown.*


# Interface Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentage` | `string` | Required | Percentage by how much the base price will increase |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServerBackup } from 'hetzner-cloud-apilib';

const serverBackup: ServerBackup = {
  percentage: '20.0000000000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



