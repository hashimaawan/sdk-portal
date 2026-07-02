# V2 Kubernetes Clusters Clusterlint Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompletedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was completed. |
| `Diagnostics` | [`List<Diagnostic>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/diagnostic.md) | Optional | An array of diagnostics reporting potential problems for the given cluster. |
| `RequestedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was made. |
| `RunId` | `string` | Optional | Id of the clusterlint run that can be used later to fetch the diagnostics. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2KubernetesClustersClusterlintResponse v2KubernetesClustersClusterlintResponse = new V2KubernetesClustersClusterlintResponse
{
    CompletedAt = DateTime.ParseExact("2019-10-30T05:34:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Diagnostics = new List<Diagnostic>
    {
        new Diagnostic
        {
            CheckName = "check_name8",
            Message = "message2",
            MObject = new MObject
            {
                Kind = "kind0",
                Name = "name2",
                MNamespace = "namespace0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Severity = "severity2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Diagnostic
        {
            CheckName = "check_name8",
            Message = "message2",
            MObject = new MObject
            {
                Kind = "kind0",
                Name = "name2",
                MNamespace = "namespace0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Severity = "severity2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    RequestedAt = DateTime.ParseExact("2019-10-30T05:34:07Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    RunId = "50c2f44c-011d-493e-aee5-361a4a0d1844",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



