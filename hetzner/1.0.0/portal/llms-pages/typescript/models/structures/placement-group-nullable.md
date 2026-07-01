# Placement Group Nullable

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwTnVsbGFibGU

*This model accepts additional fields of type unknown.*


# Interface Name

`PlacementGroupNullable`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `number` | Required | ID of the Resource |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `servers` | `number[]` | Required | Array of IDs of Servers that are part of this Placement Group |
| `type` | `string` | Required, Constant | Type of the Placement Group<br><br>**Value**: `'spread'` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PlacementGroupNullable } from 'hetzner-cloud-apilib';

const placementGroupNullable: PlacementGroupNullable = {
  created: '2016-01-30T23:55:00+00:00',
  id: 42,
  labels: {
    'key0': 'labels2'
  },
  name: 'my-resource',
  servers: [
    42
  ],
  type: 'spread',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



