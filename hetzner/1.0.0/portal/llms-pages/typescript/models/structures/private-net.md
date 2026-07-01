# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `string \| undefined` | Optional | - |
| `network` | `number \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PrivateNet } from 'hetzner-cloud-apilib';

const privateNet: PrivateNet = {
  ip: '10.0.0.2',
  network: 4711,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



