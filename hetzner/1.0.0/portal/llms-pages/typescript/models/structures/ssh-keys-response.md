# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U


# Interface Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `sshKeys` | [`SshKey[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ssh-key.md) | Required | - |


# Example

```ts
import { SshKeysResponse } from 'hetzner-cloud-apilib';

const sshKeysResponse: SshKeysResponse = {
  sshKeys: [
    {
      created: '2016-01-30T23:55:00+00:00',
      fingerprint: 'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
      id: 42,
      labels: {
        'key0': 'labels4',
        'key1': 'labels5',
        'key2': 'labels6'
      },
      name: 'my-resource',
      publicKey: 'ssh-rsa AAAjjk76kgf...Xt',
    }
  ],
  meta: {
    pagination: {
      lastPage: 77.7,
      nextPage: 209.18,
      page: 17.58,
      perPage: 13.34,
      previousPage: 50.02,
      totalEntries: 206.64,
    },
  },
};
```



