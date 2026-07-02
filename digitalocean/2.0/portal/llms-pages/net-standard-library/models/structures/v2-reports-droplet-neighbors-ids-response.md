# V2 Reports Droplet Neighbors Ids Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBSZXBvcnRzJTI1MjBEcm9wbGV0JTI1MjBOZWlnaGJvcnMlMjUyMElkcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2ReportsDropletNeighborsIdsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NeighborIds` | `List<List<int>>` | Optional | An array of arrays. Each array will contain a set of Droplet IDs for Droplets that share a physical server. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2ReportsDropletNeighborsIdsResponse v2ReportsDropletNeighborsIdsResponse = new V2ReportsDropletNeighborsIdsResponse
{
    NeighborIds = new List<List<int>>
    {
        new List<int>
        {
            168671828,
            168663509,
            168671815,
        },
        new List<int>
        {
            168671883,
            168671750,
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



