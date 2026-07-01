# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE


# Interface Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | [`Network \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/network.md) | Optional | - |


# Example

```ts
import { NetworksResponse1, Type42Enum } from 'hetzner-cloud-apilib';

const networksResponse1: NetworksResponse1 = {
  network: {
    created: 'created4',
    id: 78,
    ipRange: 'ip_range6',
    labels: { 'key1': 'val1', 'key2': 'val2' },
    name: 'name4',
    protection: {
      mDelete: false,
    },
    routes: [
      {
        destination: 'destination8',
        gateway: 'gateway6',
      },
      {
        destination: 'destination8',
        gateway: 'gateway6',
      },
      {
        destination: 'destination8',
        gateway: 'gateway6',
      }
    ],
    servers: [
      93
    ],
    subnets: [
      {
        gateway: 'gateway4',
        networkZone: 'network_zone2',
        type: Type42Enum.Cloud,
        ipRange: 'ip_range6',
      }
    ],
    loadBalancers: [
      208
    ],
  },
};
```



