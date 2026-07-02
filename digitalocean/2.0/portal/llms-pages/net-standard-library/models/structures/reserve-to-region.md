# Reserve to Region

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ReserveToRegion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ProjectId` | `Guid?` | Optional | The UUID of the project to which the floating IP will be assigned. |
| `Region` | `string` | Required | The slug identifier for the region the floating IP will be reserved to. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

ReserveToRegion reserveToRegion = new ReserveToRegion
{
    Region = "nyc3",
    ProjectId = new Guid("746c6152-2fa2-11ed-92d3-27aaa54e4988"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



