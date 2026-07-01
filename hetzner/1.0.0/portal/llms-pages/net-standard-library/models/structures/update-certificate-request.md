# Update Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZUNlcnRpZmljYXRlUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`UpdateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Optional | New Certificate name |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

UpdateCertificateRequest updateCertificateRequest = new UpdateCertificateRequest
{
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Name = "my website cert",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



