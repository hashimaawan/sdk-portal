# V2 Apps Components Logs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBDb21wb25lbnRzJTI1MjBMb2dzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsComponentsLogsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HistoricUrls` | `List<string>` | Optional | - |
| `LiveUrl` | `string` | Optional | A URL of the real-time live logs. This URL may use either the `https://` or `wss://` protocols and will keep pushing live logs as they become available. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2AppsComponentsLogsResponse v2AppsComponentsLogsResponse = new V2AppsComponentsLogsResponse
{
    HistoricUrls = new List<string>
    {
        "historic_urls9",
        "historic_urls0",
        "historic_urls1",
    },
    LiveUrl = "ws://logs/build",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



