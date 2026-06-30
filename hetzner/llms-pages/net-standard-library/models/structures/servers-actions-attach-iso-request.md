# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Iso` | `string` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ServersActionsAttachIsoRequest serversActionsAttachIsoRequest = new ServersActionsAttachIsoRequest
{
    Iso = "FreeBSD-11.0-RELEASE-amd64-dvd1",
};
```



