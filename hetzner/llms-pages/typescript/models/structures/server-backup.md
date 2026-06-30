# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage


# Interface Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentage` | `string` | Required | Percentage by how much the base price will increase |


# Example

```ts
import { ServerBackup } from 'hetzner-cloud-apilib';

const serverBackup: ServerBackup = {
  percentage: '20.0000000000',
};
```



