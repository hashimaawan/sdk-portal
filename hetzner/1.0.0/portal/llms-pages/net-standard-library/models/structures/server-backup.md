# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage

*This model accepts additional fields of type object.*


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Percentage` | `string` | Required | Percentage by how much the base price will increase |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

ServerBackup serverBackup = new ServerBackup
{
    Percentage = "20.0000000000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



