# V2 Apps Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `App` | [`AListOfApp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/a-list-of-app.md) | Optional | An application's configuration and status. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2AppsResponse1 v2AppsResponse1 = new V2AppsResponse1
{
    App = new AListOfApp
    {
        Spec = new AppSpec
        {
            Name = "name2",
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
            Region = Region1.Blr,
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
        CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        DefaultIngress = "default_ingress8",
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
        Id = "id2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



