# V2 Apps Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ProjectId` | `string` | Optional | The ID of the project the app should be assigned to. If omitted, it will be assigned to your default project. |
| `Spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2AppsRequest v2AppsRequest = new V2AppsRequest
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
    ProjectId = "project_id4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



