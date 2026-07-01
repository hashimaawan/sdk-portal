# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0


# Interface Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `aliasIps` | `string[] \| undefined` | Optional | - |
| `ip` | `string \| undefined` | Optional | - |
| `macAddress` | `string \| undefined` | Optional | - |
| `network` | `number \| undefined` | Optional | - |


# Example

```ts
import { PrivateNet4 } from 'hetzner-cloud-apilib';

const privateNet4: PrivateNet4 = {
  aliasIps: [
    'alias_ips0',
    'alias_ips9'
  ],
  ip: '10.0.0.2',
  macAddress: '86:00:ff:2a:7d:e1',
  network: 4711,
};
```



