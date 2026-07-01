# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`NullableAction \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/nullable-action.md) | Optional | - |
| `placementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/placement-group.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreatePlacementGroupResponse, Status } from 'hetzner-cloud-apilib';

const createPlacementGroupResponse: CreatePlacementGroupResponse = {
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
  action: {
    command: 'command6',
    error: {
      code: 'code2',
      message: 'message4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    finished: 'finished0',
    id: 238,
    progress: 143.26,
    resources: [
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    started: 'started8',
    status: Status.Running,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



