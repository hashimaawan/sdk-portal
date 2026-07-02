# Assign to Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwdG8lMjUyMERyb3BsZXQx

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`AssignToDroplet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletId` | `int` | Required | The ID of the Droplet that the reserved IP will be assigned to. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

AssignToDroplet1 assignToDroplet1 = new AssignToDroplet1
{
    DropletId = 2457247,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



