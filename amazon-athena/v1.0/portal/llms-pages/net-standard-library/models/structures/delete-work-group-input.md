# Delete Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRlbGV0ZVdvcmtHcm91cElucHV0


# Class Name

`DeleteWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `RecursiveDeleteOption` | `bool?` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

DeleteWorkGroupInput deleteWorkGroupInput = new DeleteWorkGroupInput
{
    WorkGroup = "WorkGroup0",
    RecursiveDeleteOption = false,
};
```



