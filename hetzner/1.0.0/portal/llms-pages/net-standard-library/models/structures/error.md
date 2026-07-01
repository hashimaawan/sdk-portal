# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Code` | `string` | Required | Fixed machine readable code |
| `Message` | `string` | Required | Humanized error message |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Error error = new Error
{
    Code = "action_failed",
    Message = "Action failed",
};
```



