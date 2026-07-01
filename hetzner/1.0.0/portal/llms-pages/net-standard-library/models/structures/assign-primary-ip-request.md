# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q


# Class Name

`AssignPrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `int` | Required | ID of a resource of type `assignee_type` |
| `AssigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

AssignPrimaryIPRequest assignPrimaryIPRequest = new AssignPrimaryIPRequest
{
    AssigneeId = 4711,
    AssigneeType = "server",
};
```



