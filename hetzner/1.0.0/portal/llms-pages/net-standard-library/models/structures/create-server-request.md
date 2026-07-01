# Create Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`CreateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `bool?` | Optional | Auto-mount Volumes after attach |
| `Datacenter` | `string` | Optional | ID or name of Datacenter to create Server in (must not be used together with location) |
| `Firewalls` | [`List<Firewall4>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall-4.md) | Optional | Firewalls which should be applied on the Server's public network interface at creation time |
| `Image` | `string` | Required | ID or name of the Image the Server is created from |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Location` | `string` | Optional | ID or name of Location to create Server in (must not be used together with datacenter) |
| `Name` | `string` | Required | Name of the Server to create (must be unique per Project and a valid hostname as per RFC 1123) |
| `Networks` | `List<int>` | Optional | Network IDs which should be attached to the Server private network interface at the creation time |
| `PlacementGroup` | `int?` | Optional | ID of the Placement Group the server should be in |
| `PublicNet` | [`PublicNet5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/public-net-5.md) | Optional | Public Network options |
| `ServerType` | `string` | Required | ID or name of the Server type this Server should be created with |
| `SshKeys` | `List<string>` | Optional | SSH key IDs (`integer`) or names (`string`) which should be injected into the Server at creation time |
| `StartAfterCreate` | `bool?` | Optional | Start Server right after creation. Defaults to true. |
| `UserData` | `string` | Optional | Cloud-Init user data to use during Server creation. This field is limited to 32KiB. |
| `Volumes` | `List<int>` | Optional | Volume IDs which should be attached to the Server at the creation time. Volumes must be in the same Location. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

CreateServerRequest createServerRequest = new CreateServerRequest
{
    Image = "ubuntu-20.04",
    Name = "my-server",
    ServerType = "cx11",
    Automount = false,
    Datacenter = "nbg1-dc3",
    Firewalls = new List<Firewall4>
    {
        new Firewall4
        {
            Firewall = 38,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    Location = "nbg1",
    Networks = new List<int>
    {
        456,
    },
    PlacementGroup = 1,
    SshKeys = new List<string>
    {
        "my-ssh-key",
    },
    StartAfterCreate = true,
    UserData = "#cloud-config\nruncmd:\n- [touch, /root/cloud-init-worked]\n",
    Volumes = new List<int>
    {
        123,
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



