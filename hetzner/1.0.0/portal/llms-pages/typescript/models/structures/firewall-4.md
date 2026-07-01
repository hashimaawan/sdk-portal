# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxsNA

*This model accepts additional fields of type unknown.*


# Interface Name

`Firewall4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewall` | `number \| undefined` | Optional | ID of the Firewall |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Firewall4 } from 'hetzner-cloud-apilib';

const firewall4: Firewall4 = {
  firewall: 176,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



