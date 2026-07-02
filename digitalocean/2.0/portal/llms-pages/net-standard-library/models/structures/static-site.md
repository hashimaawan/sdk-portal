# Static Site

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXRpY1NpdGU

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`StaticSite`


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
| `CatchallDocument` | `string` | Optional | The name of the document to use as the fallback for any requests to documents that are not found when serving this static site. Only 1 of `catchall_document` or `error_document` can be set. |
| `Cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/cors.md) | Optional | - |
| `ErrorDocument` | `string` | Optional | The name of the error document to use when serving this static site. Default: 404.html. If no such file exists within the built assets, App Platform will supply one.<br><br>**Default**: `"404.html"` |
| `IndexDocument` | `string` | Optional | The name of the index document to use when serving this static site. Default: index.html<br><br>**Default**: `"index.html"` |
| `OutputDir` | `string` | Optional | An optional path to where the built assets will be located, relative to the build context. If not set, App Platform will automatically scan for these directory names: `_static`, `dist`, `public`, `build`. |
| `Routes` | [`List<ACriterionForRoutingHttpTrafficToAComponent>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

StaticSite staticSite = new StaticSite
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
    RunCommand = "bin/api",
    SourceDir = "path/to/dir",
    CatchallDocument = "index.html",
    ErrorDocument = "error.html",
    IndexDocument = "main.html",
    OutputDir = "dist/",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



