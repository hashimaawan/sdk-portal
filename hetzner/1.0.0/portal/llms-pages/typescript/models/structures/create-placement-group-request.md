# Create Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CreatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the PlacementGroup |
| `type` | `string` | Required, Constant | Define the Placement Group Type.<br><br>**Value**: `'spread'` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreatePlacementGroupRequest } from 'hetzner-cloud-apilib';

const createPlacementGroupRequest: CreatePlacementGroupRequest = {
  name: 'my Placement Group',
  type: 'spread',
  labels: { 'key1': 'val1', 'key2': 'val2' },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



