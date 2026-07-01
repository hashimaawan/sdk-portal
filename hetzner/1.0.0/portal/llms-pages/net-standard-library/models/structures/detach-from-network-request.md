# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | `int` | Required | ID of an existing network to detach the Server from |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

DetachFromNetworkRequest detachFromNetworkRequest = new DetachFromNetworkRequest
{
    Network = 4711,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



