# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNzaEtleQ


# Interface Name

`SshKey`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `fingerprint` | `string` | Required | Fingerprint of public key |
| `id` | `number` | Required | ID of the Resource |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `publicKey` | `string` | Required | Public key |


# Example

```ts
import { SshKey } from 'hetzner-cloud-apilib';

const sshKey: SshKey = {
  created: '2016-01-30T23:55:00+00:00',
  fingerprint: 'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
  id: 42,
  labels: {
    'key0': 'labels4',
    'key1': 'labels3',
    'key2': 'labels2'
  },
  name: 'my-resource',
  publicKey: 'ssh-rsa AAAjjk76kgf...Xt',
};
```



