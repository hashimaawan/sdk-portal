# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Iso` | `string` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

ServersActionsAttachIsoRequest serversActionsAttachIsoRequest = new ServersActionsAttachIsoRequest
{
    Iso = "FreeBSD-11.0-RELEASE-amd64-dvd1",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



