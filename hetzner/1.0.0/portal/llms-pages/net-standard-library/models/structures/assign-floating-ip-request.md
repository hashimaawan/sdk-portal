# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |


# Class Name

`AssignFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Server` | `int` | Required | ID of the Server the Floating IP shall be assigned to |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

AssignFloatingIPRequest assignFloatingIPRequest = new AssignFloatingIPRequest
{
    Server = 42,
};
```



