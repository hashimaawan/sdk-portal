# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE


# Interface Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New name Name to set |


# Example

```ts
import { SshKeysRequest1 } from 'hetzner-cloud-apilib';

const sshKeysRequest1: SshKeysRequest1 = {
  labels: { 'labelkey': 'value' },
  name: 'My ssh key',
};
```



