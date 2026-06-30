# Label Selector 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I3

Label selector and a list of selected targets


# Class Name

`LabelSelector7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Selector` | `string` | Required | Label selector |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

LabelSelector7 labelSelector7 = new LabelSelector7
{
    Selector = "env=prod",
};
```



