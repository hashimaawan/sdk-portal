# V2 Kubernetes Clusters Clusterlint Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExcludeChecks` | `List<string>` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `ExcludeGroups` | `List<string>` | Optional | An array of check groups that will be omitted when clusterlint executes checks. |
| `IncludeChecks` | `List<string>` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `IncludeGroups` | `List<string>` | Optional | An array of check groups that will be run when clusterlint executes checks. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2KubernetesClustersClusterlintRequest v2KubernetesClustersClusterlintRequest = new V2KubernetesClustersClusterlintRequest
{
    ExcludeChecks = new List<string>
    {
        "default-namespace",
    },
    ExcludeGroups = new List<string>
    {
        "workload-health",
    },
    IncludeChecks = new List<string>
    {
        "bare-pods",
        "resource-requirements",
    },
    IncludeGroups = new List<string>
    {
        "basic",
        "doks",
        "security",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



