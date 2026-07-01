# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | `string` | Required | ID or name of Image to rebuilt from. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

RebuildServerRequest rebuildServerRequest = new RebuildServerRequest
{
    Image = "ubuntu-20.04",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



