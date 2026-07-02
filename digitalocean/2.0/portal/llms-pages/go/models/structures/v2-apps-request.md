# V2 Apps Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ProjectId` | `*string` | Optional | The ID of the project the app should be assigned to. If omitted, it will be assigned to your default project. |
| `Spec` | [`models.AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2AppsRequest := models.V2AppsRequest{
        ProjectId:             models.ToPointer("project_id4"),
        Spec:                  models.AppSpec{
            Databases:             []models.Database{
                models.Database{
                    ClusterName:           models.ToPointer("cluster_name8"),
                    DbName:                models.ToPointer("db_name0"),
                    DbUser:                models.ToPointer("db_user8"),
                    Engine:                models.ToPointer(models.Engine_Pg),
                    Name:                  "name6",
                    Production:            models.ToPointer(false),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Domains:               []models.Domain{
                models.Domain{
                    Domain:                "domain6",
                    MinimumTlsVersion:     models.ToPointer(models.MinimumTlsVersion_Enum12),
                    Type:                  models.ToPointer(models.Type1_Primary),
                    Wildcard:              models.ToPointer(false),
                    Zone:                  models.ToPointer("zone2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Domain{
                    Domain:                "domain6",
                    MinimumTlsVersion:     models.ToPointer(models.MinimumTlsVersion_Enum12),
                    Type:                  models.ToPointer(models.Type1_Primary),
                    Wildcard:              models.ToPointer(false),
                    Zone:                  models.ToPointer("zone2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Functions:             []models.Function{
                models.Function{
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
                        models.Env{
                            Key:                   "key2",
                            Scope:                 models.ToPointer(models.Scope_Unset),
                            Type:                  models.ToPointer(models.Type2_General),
                            Value:                 models.ToPointer("value4"),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
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
                    Name:                  "name4",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Jobs:                  []models.Job{
                models.Job{
                    BuildCommand:          models.ToPointer("build_command8"),
                    DockerfilePath:        models.ToPointer("dockerfile_path6"),
                    EnvironmentSlug:       models.ToPointer("environment_slug2"),
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
                        models.Env{
                            Key:                   "key2",
                            Scope:                 models.ToPointer(models.Scope_Unset),
                            Type:                  models.ToPointer(models.Type2_General),
                            Value:                 models.ToPointer("value4"),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
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
                    Name:                  "name4",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Name:                  "web-app-01",
            Region:                models.ToPointer(models.Region1_Nyc),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



