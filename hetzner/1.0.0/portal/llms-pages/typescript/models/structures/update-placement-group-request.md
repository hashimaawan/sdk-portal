# Update Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Interface Name

`UpdatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New PlacementGroup name |


# Example

```ts
import { UpdatePlacementGroupRequest } from 'hetzner-cloud-apilib';

const updatePlacementGroupRequest: UpdatePlacementGroupRequest = {
  labels: { 'labelkey': 'value' },
  name: 'my Placement Group',
};
```



