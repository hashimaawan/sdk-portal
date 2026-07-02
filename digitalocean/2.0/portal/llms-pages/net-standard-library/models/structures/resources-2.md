# Resources 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc291cmNlczI

An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Resources2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Count` | `int?` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `LastTaggedUri` | `string` | Optional | The URI for the last tagged object for this type of resource. |
| `Databases` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `Droplets` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `Imgages` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `VolumeSnapshots` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `Volumes` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Resources2 resources2 = new Resources2
{
    Count = 5,
    LastTaggedUri = "https://api.digitalocean.com/v2/images/7555620",
    Databases = new Databases
    {
        Count = 1,
        LastTaggedUri = "https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Droplets = new Databases
    {
        Count = 1,
        LastTaggedUri = "https://api.digitalocean.com/v2/droplets/3164444",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Imgages = new Databases
    {
        Count = 158,
        LastTaggedUri = "last_tagged_uri4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    VolumeSnapshots = new Databases
    {
        Count = 1,
        LastTaggedUri = "https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519",
    },
    Volumes = new Databases
    {
        Count = 1,
        LastTaggedUri = "https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933",
    },
    ["images"] = ApiHelper.JsonDeserialize<object>("{\"count\":1,\"last_tagged_uri\":\"https://api.digitalocean.com/v2/images/7555620\"}"),
};
```



