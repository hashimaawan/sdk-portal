# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) |
| `rebuild` | `boolean \| undefined` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServersActionsChangeProtectionRequest } from 'hetzner-cloud-apilib';

const serversActionsChangeProtectionRequest: ServersActionsChangeProtectionRequest = {
  mDelete: true,
  rebuild: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



