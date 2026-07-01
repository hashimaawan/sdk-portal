# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE

*This model accepts additional fields of type unknown.*


# Interface Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New name Name to set |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { SshKeysRequest1 } from 'hetzner-cloud-apilib';

const sshKeysRequest1: SshKeysRequest1 = {
  labels: { 'labelkey': 'value' },
  name: 'My ssh key',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



