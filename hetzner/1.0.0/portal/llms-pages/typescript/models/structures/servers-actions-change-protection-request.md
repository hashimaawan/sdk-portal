# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Interface Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) |
| `rebuild` | `boolean \| undefined` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) |


# Example

```ts
import { ServersActionsChangeProtectionRequest } from 'hetzner-cloud-apilib';

const serversActionsChangeProtectionRequest: ServersActionsChangeProtectionRequest = {
  mDelete: true,
  rebuild: true,
};
```



