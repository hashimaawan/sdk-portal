# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Interface Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/placement-group.md) | Required | - |


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
  },
};
```



