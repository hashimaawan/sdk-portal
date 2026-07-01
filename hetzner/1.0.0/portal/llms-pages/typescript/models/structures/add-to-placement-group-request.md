# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0


# Interface Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placementGroup` | `number` | Required | ID of Placement Group the Server should be added to |


# Example

```ts
import { AddToPlacementGroupRequest } from 'hetzner-cloud-apilib';

const addToPlacementGroupRequest: AddToPlacementGroupRequest = {
  placementGroup: 1,
};
```



