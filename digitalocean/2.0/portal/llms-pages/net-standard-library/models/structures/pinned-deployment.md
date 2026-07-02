# Pinned Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBpbm5lZERlcGxveW1lbnQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`PinnedDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cause` | `string` | Optional | - |
| `ClonedFrom` | `string` | Optional | - |
| `CreatedAt` | `DateTime?` | Optional | - |
| `Functions` | [`List<FunctionsComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/functions-components-that-are-part-of-this-deployment.md) | Optional | - |
| `Id` | `string` | Optional | - |
| `Jobs` | [`List<JobComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/job-components-that-are-part-of-this-deployment.md) | Optional | - |
| `Phase` | [`Phase?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/phase.md) | Optional | **Default**: `Phase.UNKNOWN` |
| `PhaseLastUpdatedAt` | `DateTime?` | Optional | - |
| `Progress` | [`Progress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/progress.md) | Optional | - |
| `Services` | [`List<ServiceComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/service-components-that-are-part-of-this-deployment.md) | Optional | - |
| `Spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `StaticSites` | [`List<StaticSiteComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/static-site-components-that-are-part-of-this-deployment.md) | Optional | - |
| `TierSlug` | `string` | Optional, Read-only | - |
| `UpdatedAt` | `DateTime?` | Optional | - |
| `Workers` | [`List<WorkerComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/worker-components-that-are-part-of-this-deployment.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

PinnedDeployment pinnedDeployment = new PinnedDeployment
{
    Cause = "commit 9a4df0b pushed to github/digitalocean/sample-golang",
    ClonedFrom = "3aa4d20e-5527-4c00-b496-601fbd22520a",
    CreatedAt = DateTime.ParseExact("2020-07-28T18:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Functions = new List<FunctionsComponentsThatArePartOfThisDeployment>
    {
        new FunctionsComponentsThatArePartOfThisDeployment
        {
            Name = "name4",
            MNamespace = "namespace8",
            SourceCommitHash = "source_commit_hash4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new FunctionsComponentsThatArePartOfThisDeployment
        {
            Name = "name4",
            MNamespace = "namespace8",
            SourceCommitHash = "source_commit_hash4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new FunctionsComponentsThatArePartOfThisDeployment
        {
            Name = "name4",
            MNamespace = "namespace8",
            SourceCommitHash = "source_commit_hash4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Id = "b6bdf840-2854-4f87-a36c-5f231c617c84",
    Phase = Phase.Active,
    PhaseLastUpdatedAt = DateTime.ParseExact("0001-01-01T00:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    TierSlug = "basic",
    UpdatedAt = DateTime.ParseExact("2020-07-28T18:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



