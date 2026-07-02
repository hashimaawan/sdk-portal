# Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZpY2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Service`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BuildCommand` | `*string` | Optional | An optional build command to run while building this component from source. |
| `DockerfilePath` | `*string` | Optional | The path to the Dockerfile relative to the root of the repo. If set, it will be used to build this component. Otherwise, App Platform will attempt to build it using buildpacks. |
| `EnvironmentSlug` | `*string` | Optional | An environment slug describing the type of this app. For a full list, please refer to [the product documentation](https://www.digitalocean.com/docs/app-platform/). |
| `Envs` | [`[]models.Env`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `Git` | [`*models.Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/git.md) | Optional | - |
| `Github` | [`*models.Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/github.md) | Optional | - |
| `Gitlab` | [`*models.Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/gitlab.md) | Optional | - |
| `Image` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `LogDestinations` | [`*models.ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/configurations-for-external-logging.md) | Optional | - |
| `Name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `RunCommand` | `*string` | Optional | An optional run command to override the component's default. |
| `SourceDir` | `*string` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `InstanceCount` | `*int64` | Optional | The amount of instances that this component should be scaled to. Default: 1<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `InstanceSizeSlug` | [`*models.InstanceSizeSlug`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/instance-size-slug.md) | Optional | The instance size to use for this component. Default: `basic-xxs`<br><br>**Default**: `"basic-xxs"` |
| `Cors` | [`*models.Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/cors.md) | Optional | - |
| `HealthCheck` | [`*models.HealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/health-check.md) | Optional | - |
| `HttpPort` | `*int64` | Optional | The internal port on which this service's run command will listen. Default: 8080<br>If there is not an environment variable with the name `PORT`, one will be automatically added with its value set to the value of this field.<br><br>**Constraints**: `>= 1`, `<= 65535` |
| `InternalPorts` | `[]int64` | Optional | The ports on which this service will listen for internal traffic. |
| `Routes` | [`[]models.ACriterionForRoutingHttpTrafficToAComponent`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    service := models.Service{
        BuildCommand:          models.ToPointer("npm run build"),
        DockerfilePath:        models.ToPointer("path/to/Dockerfile"),
        EnvironmentSlug:       models.ToPointer("node-js"),
        Envs:                  []models.Env{
            models.Env{
                Key:                   "key2",
                Scope:                 models.ToPointer(models.Scope_Unset),
                Type:                  models.ToPointer(models.Type2_General),
                Value:                 models.ToPointer("value4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Git:                   models.ToPointer(models.Git{
            Branch:                models.ToPointer("branch8"),
            RepoCloneUrl:          models.ToPointer("repo_clone_url8"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Name:                  "api",
        RunCommand:            models.ToPointer("bin/api"),
        SourceDir:             models.ToPointer("path/to/dir"),
        InstanceCount:         models.ToPointer(int64(2)),
        InstanceSizeSlug:      models.ToPointer(models.InstanceSizeSlug_Basicxxs),
        HttpPort:              models.ToPointer(int64(3000)),
        InternalPorts:         []int64{
            int64(80),
            int64(443),
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



