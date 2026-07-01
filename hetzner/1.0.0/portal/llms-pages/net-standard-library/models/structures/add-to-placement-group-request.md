# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PlacementGroup` | `int` | Required | ID of Placement Group the Server should be added to |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

AddToPlacementGroupRequest addToPlacementGroupRequest = new AddToPlacementGroupRequest
{
    PlacementGroup = 1,
};
```



