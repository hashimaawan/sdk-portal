# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/placement-group.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PlacementGroupResponse } from 'hetzner-cloud-apilib';

const placementGroupResponse: PlacementGroupResponse = {
  placementGroup: {
    created: '2016-01-30T23:55:00+00:00',
    id: 42,
    labels: {
      'key0': 'labels4'
    },
    name: 'my-resource',
    servers: [
      42
    ],
    type: 'spread',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



