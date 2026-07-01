# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `number` | Required | ID of an existing network to detach the Server from |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DetachFromNetworkRequest } from 'hetzner-cloud-apilib';

const detachFromNetworkRequest: DetachFromNetworkRequest = {
  network: 4711,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



