# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `placementGroups` | [`PlacementGroup[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/placement-group.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PlacementGroupsResponse } from 'hetzner-cloud-apilib';

const placementGroupsResponse: PlacementGroupsResponse = {
  placementGroups: [
    {
      created: '2016-01-30T23:55:00+00:00',
      id: 42,
      labels: {
        'key0': 'labels0',
        'key1': 'labels1'
      },
      name: 'my-resource',
      servers: [
        42
      ],
      type: 'spread',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
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
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



