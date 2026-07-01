# Label Selector 12

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3IxMg

Configuration for label selector targets, required if type is `label_selector`


# Class Name

`LabelSelector12`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Selector` | `string` | Required | Label selector |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

LabelSelector12 labelSelector12 = new LabelSelector12
{
    Selector = "env=prod",
};
```



