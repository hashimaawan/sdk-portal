# A List of App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkElMjUyMGxpc3QlMjUyMG9mJTI1MjBhcHA

An application's configuration and status.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`AListOfApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ActiveDeployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/an-app-deployment.md) | Optional | - |
| `CreatedAt` | `DateTime?` | Optional, Read-only | - |
| `DefaultIngress` | `string` | Optional, Read-only | - |
| `Domains` | [`List<ContainsAllDomainsForTheApp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/contains-all-domains-for-the-app.md) | Optional, Read-only | - |
| `Id` | `string` | Optional, Read-only | - |
| `InProgressDeployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/an-app-deployment.md) | Optional | - |
| `LastDeploymentCreatedAt` | `DateTime?` | Optional, Read-only | - |
| `LiveDomain` | `string` | Optional, Read-only | - |
| `LiveUrl` | `string` | Optional, Read-only | - |
| `LiveUrlBase` | `string` | Optional, Read-only | - |
| `OwnerUuid` | `string` | Optional, Read-only | - |
| `PendingDeployment` | [`PendingDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/pending-deployment.md) | Optional | - |
| `PinnedDeployment` | [`PinnedDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/pinned-deployment.md) | Optional | - |
| `ProjectId` | `string` | Optional, Read-only | - |
| `Region` | [`GeographicalInformationAboutAnAppOrigin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/geographical-information-about-an-app-origin.md) | Optional | - |
| `Spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `TierSlug` | `string` | Optional, Read-only | - |
| `UpdatedAt` | `DateTime?` | Optional, Read-only | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

AListOfApp aListOfApp = new AListOfApp
{
    Spec = new AppSpec
    {
        Name = "web-app-01",
        Databases = new List<Database>
        {
            new Database
            {
                Name = "name6",
                ClusterName = "cluster_name8",
                DbName = "db_name0",
                DbUser = "db_user8",
                Engine = Engine.Pg,
                Production = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Domains = new List<Domain>
        {
            new Domain
            {
                DomainProp = "domain6",
                MinimumTlsVersion = MinimumTlsVersion.Enum12,
                Type = Type1.Primary,
                Wildcard = false,
                Zone = "zone2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Domain
            {
                DomainProp = "domain6",
                MinimumTlsVersion = MinimumTlsVersion.Enum12,
                Type = Type1.Primary,
                Wildcard = false,
                Zone = "zone2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Functions = new List<Function>
        {
            new Function
            {
                Name = "name4",
                Alerts = new List<Alert>
                {
                    new Alert
                    {
                        Disabled = false,
                        MOperator = Operator.LessThan,
                        Rule = Rule.MemUtilization,
                        MValue = 12.58,
                        Window = Window.ThirtyMinutes,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Cors = new Cors
                {
                    AllowCredentials = false,
                    AllowHeaders = new List<string>
                    {
                        "allow_headers9",
                        "allow_headers0",
                    },
                    AllowMethods = new List<string>
                    {
                        "allow_methods8",
                        "allow_methods9",
                        "allow_methods0",
                    },
                    AllowOrigins = new List<AllowOrigin>
                    {
                        null,
                    },
                    ExposeHeaders = new List<string>
                    {
                        "expose_headers2",
                    },
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Envs = new List<Env>
                {
                    new Env
                    {
                        Key = "key2",
                        Scope = Scope.Unset,
                        Type = Type2.General,
                        MValue = "value4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new Env
                    {
                        Key = "key2",
                        Scope = Scope.Unset,
                        Type = Type2.General,
                        MValue = "value4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new Env
                    {
                        Key = "key2",
                        Scope = Scope.Unset,
                        Type = Type2.General,
                        MValue = "value4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Git = new Git
                {
                    Branch = "branch8",
                    RepoCloneUrl = "repo_clone_url8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Github = new Github
                {
                    Branch = "branch4",
                    DeployOnPush = false,
                    Repo = "repo6",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Jobs = new List<Job>
        {
            new Job
            {
                Name = "name4",
                BuildCommand = "build_command8",
                DockerfilePath = "dockerfile_path6",
                EnvironmentSlug = "environment_slug2",
                Envs = new List<Env>
                {
                    new Env
                    {
                        Key = "key2",
                        Scope = Scope.Unset,
                        Type = Type2.General,
                        MValue = "value4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new Env
                    {
                        Key = "key2",
                        Scope = Scope.Unset,
                        Type = Type2.General,
                        MValue = "value4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new Env
                    {
                        Key = "key2",
                        Scope = Scope.Unset,
                        Type = Type2.General,
                        MValue = "value4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Git = new Git
                {
                    Branch = "branch8",
                    RepoCloneUrl = "repo_clone_url8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Region = Region1.Nyc,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ActiveDeployment = new AnAppDeployment
    {
        Cause = "cause6",
        ClonedFrom = "cloned_from2",
        CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
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
        Id = "id0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    CreatedAt = DateTime.ParseExact("2020-11-19T20:27:18Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    DefaultIngress = "digitalocean.com",
    Domains = new List<ContainsAllDomainsForTheApp>
    {
        new ContainsAllDomainsForTheApp
        {
            CertificateExpiresAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Id = "id0",
            Phase = Phase1.Configuring,
            Progress = new Progress1
            {
                Steps = new List<object>
                {
                    ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            RotateValidationRecords = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Id = "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    LastDeploymentCreatedAt = DateTime.ParseExact("2020-11-19T20:27:18Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    LiveDomain = "live_domain",
    LiveUrl = "google.com",
    LiveUrlBase = "digitalocean.com",
    OwnerUuid = "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    ProjectId = "88b72d1a-b78a-4d9f-9090-b53c4399073f",
    TierSlug = "basic",
    UpdatedAt = DateTime.ParseExact("2020-12-01T00:42:16Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



