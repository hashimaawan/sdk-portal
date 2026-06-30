# Ssh Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2Ux


# Interface Name

`SshKeysResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sshKey` | [`SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/ssh-key.md) | Required | - |


# Example

```ts
import { SshKeysResponse1 } from 'hetzner-cloud-apilib';

const sshKeysResponse1: SshKeysResponse1 = {
  sshKey: {
    created: '2016-01-30T23:55:00+00:00',
    fingerprint: 'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
    id: 42,
    labels: {
      'key0': 'labels0'
    },
    name: 'my-resource',
    publicKey: 'ssh-rsa AAAjjk76kgf...Xt',
  },
};
```



