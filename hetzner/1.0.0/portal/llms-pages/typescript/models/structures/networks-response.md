# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ


# Interface Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `networks` | [`Network[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/network.md) | Required | - |


# Example

```ts
import { NetworksResponse, Type42Enum } from 'hetzner-cloud-apilib';

const networksResponse: NetworksResponse = {
  networks: [
    {
      created: '2016-01-30T23:50:00+00:00',
      id: 4711,
      ipRange: '10.0.0.0/16',
      labels: { 'key1': 'val1', 'key2': 'val2' },
      name: 'mynet',
      protection: {
        mDelete: false,
      },
      routes: [
        {
          destination: '10.100.1.0/24',
          gateway: '10.0.1.1',
        }
      ],
      servers: [
        42
      ],
      subnets: [
        {
          gateway: '10.0.0.1',
          networkZone: 'eu-central',
          type: Type42Enum.Cloud,
          ipRange: '10.0.1.0/24',
        }
      ],
      loadBalancers: [
        42
      ],
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



