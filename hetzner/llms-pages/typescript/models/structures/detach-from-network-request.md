# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA


# Interface Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `number` | Required | ID of an existing network to detach the Server from |


# Example

```ts
import { DetachFromNetworkRequest } from 'hetzner-cloud-apilib';

const detachFromNetworkRequest: DetachFromNetworkRequest = {
  network: 4711,
};
```



