# Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZpY2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Service`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BuildCommand` | `string` | Optional | An optional build command to run while building this component from source. |
| `DockerfilePath` | `string` | Optional | The path to the Dockerfile relative to the root of the repo. If set, it will be used to build this component. Otherwise, App Platform will attempt to build it using buildpacks. |
| `EnvironmentSlug` | `string` | Optional | An environment slug describing the type of this app. For a full list, please refer to [the product documentation](https://www.digitalocean.com/docs/app-platform/). |
| `Envs` | [`List<Env>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `Git` | [`Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/git.md) | Optional | - |
| `Github` | [`Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/github.md) | Optional | - |
| `Gitlab` | [`Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/gitlab.md) | Optional | - |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `LogDestinations` | [`ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/configurations-for-external-logging.md) | Optional | - |
| `Name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `RunCommand` | `string` | Optional | An optional run command to override the component's default. |
| `SourceDir` | `string` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `InstanceCount` | `long?` | Optional | The amount of instances that this component should be scaled to. Default: 1<br><br>**Default**: `1L`<br><br>**Constraints**: `>= 1` |
| `InstanceSizeSlug` | [`InstanceSizeSlug?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/instance-size-slug.md) | Optional | The instance size to use for this component. Default: `basic-xxs`<br><br>**Default**: `InstanceSizeSlug.basicxxs` |
| `Cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/cors.md) | Optional | - |
| `HealthCheck` | [`HealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/health-check.md) | Optional | - |
| `HttpPort` | `long?` | Optional | The internal port on which this service's run command will listen. Default: 8080<br>If there is not an environment variable with the name `PORT`, one will be automatically added with its value set to the value of this field.<br><br>**Constraints**: `>= 1`, `<= 65535` |
| `InternalPorts` | `List<long>` | Optional | The ports on which this service will listen for internal traffic. |
| `Routes` | [`List<ACriterionForRoutingHttpTrafficToAComponent>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Service service = new Service
{
    Name = "api",
    BuildCommand = "npm run build",
    DockerfilePath = "path/to/Dockerfile",
    EnvironmentSlug = "node-js",
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
    },
    Git = new Git
    {
        Branch = "branch8",
        RepoCloneUrl = "repo_clone_url8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    RunCommand = "bin/api",
    SourceDir = "path/to/dir",
    InstanceCount = 2L,
    InstanceSizeSlug = InstanceSizeSlug.Basicxxs,
    HttpPort = 3000L,
    InternalPorts = new List<long>
    {
        80L,
        443L,
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



