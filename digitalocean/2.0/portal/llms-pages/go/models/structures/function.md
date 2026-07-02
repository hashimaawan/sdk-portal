# Function

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkZ1bmN0aW9u

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Function`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alerts` | [`[]models.Alert`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/alert.md) | Optional | - |
| `Cors` | [`*models.Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/cors.md) | Optional | - |
| `Envs` | [`[]models.Env`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `Git` | [`*models.Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/git.md) | Optional | - |
| `Github` | [`*models.Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/github.md) | Optional | - |
| `Gitlab` | [`*models.Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/gitlab.md) | Optional | - |
| `LogDestinations` | [`*models.ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/configurations-for-external-logging.md) | Optional | - |
| `Name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `Routes` | [`[]models.ACriterionForRoutingHttpTrafficToAComponent`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `SourceDir` | `*string` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    function := models.Function{
        Alerts:                []models.Alert{
            models.Alert{
                Disabled:              models.ToPointer(false),
                Operator:              models.ToPointer(models.Operator_LessThan),
                Rule:                  models.ToPointer(models.Rule_MemUtilization),
                Value:                 models.ToPointer(float64(12.58)),
                Window:                models.ToPointer(models.Window_ThirtyMinutes),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Alert{
                Disabled:              models.ToPointer(false),
                Operator:              models.ToPointer(models.Operator_LessThan),
                Rule:                  models.ToPointer(models.Rule_MemUtilization),
                Value:                 models.ToPointer(float64(12.58)),
                Window:                models.ToPointer(models.Window_ThirtyMinutes),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Cors:                  models.ToPointer(models.Cors{
            AllowCredentials:      models.ToPointer(false),
            AllowHeaders:          []string{
                "allow_headers9",
                "allow_headers0",
            },
            AllowMethods:          []string{
                "allow_methods8",
                "allow_methods9",
                "allow_methods0",
            },
            AllowOrigins:          []models.AllowOrigin{
                nil,
            },
            ExposeHeaders:         []string{
                "expose_headers2",
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
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
        Github:                models.ToPointer(models.Github{
            Branch:                models.ToPointer("branch4"),
            DeployOnPush:          models.ToPointer(false),
            Repo:                  models.ToPointer("repo6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Name:                  "api",
        SourceDir:             models.ToPointer("path/to/dir"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



