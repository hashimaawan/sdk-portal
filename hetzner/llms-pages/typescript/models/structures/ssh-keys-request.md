# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA


# Interface Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the SSH key |
| `publicKey` | `string` | Required | Public key |


# Example

```ts
import { SshKeysRequest } from 'hetzner-cloud-apilib';

const sshKeysRequest: SshKeysRequest = {
  name: 'My ssh key',
  publicKey: 'ssh-rsa AAAjjk76kgf...Xt',
  labels: { 'key1': 'val1', 'key2': 'val2' },
};
```



