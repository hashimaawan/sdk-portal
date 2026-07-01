# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SshKeys` | `List<int>` | Optional | Array of SSH key IDs which should be injected into the rescue system. |
| `Type` | [`Type65?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

ServersActionsEnableRescueRequest serversActionsEnableRescueRequest = new ServersActionsEnableRescueRequest
{
    SshKeys = new List<int>
    {
        2323,
    },
    Type = Type65.Linux64,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



