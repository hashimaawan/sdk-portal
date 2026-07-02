# A List of App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkElMjUyMGxpc3QlMjUyMG9mJTI1MjBhcHA

An application's configuration and status.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`AListOfApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ActiveDeployment` | [`*models.AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/an-app-deployment.md) | Optional | - |
| `CreatedAt` | `*time.Time` | Optional, Read-only | - |
| `DefaultIngress` | `*string` | Optional, Read-only | - |
| `Domains` | [`[]models.ContainsAllDomainsForTheApp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/contains-all-domains-for-the-app.md) | Optional, Read-only | - |
| `Id` | `*string` | Optional, Read-only | - |
| `InProgressDeployment` | [`*models.AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/an-app-deployment.md) | Optional | - |
| `LastDeploymentCreatedAt` | `*time.Time` | Optional, Read-only | - |
| `LiveDomain` | `*string` | Optional, Read-only | - |
| `LiveUrl` | `*string` | Optional, Read-only | - |
| `LiveUrlBase` | `*string` | Optional, Read-only | - |
| `OwnerUuid` | `*string` | Optional, Read-only | - |
| `PendingDeployment` | [`*models.PendingDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pending-deployment.md) | Optional | - |
| `PinnedDeployment` | [`*models.PinnedDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pinned-deployment.md) | Optional | - |
| `ProjectId` | `*string` | Optional, Read-only | - |
| `Region` | [`*models.GeographicalInformationAboutAnAppOrigin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/geographical-information-about-an-app-origin.md) | Optional | - |
| `Spec` | [`models.AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `TierSlug` | `*string` | Optional, Read-only | - |
| `UpdatedAt` | `*time.Time` | Optional, Read-only | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    aListOfApp := models.AListOfApp{
        ActiveDeployment:        models.ToPointer(models.AnAppDeployment{
            Cause:                 models.ToPointer("cause6"),
            ClonedFrom:            models.ToPointer("cloned_from2"),
            CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            Functions:             []models.FunctionsComponentsThatArePartOfThisDeployment{
                models.FunctionsComponentsThatArePartOfThisDeployment{
                    Name:                  models.ToPointer("name4"),
                    Namespace:             models.ToPointer("namespace8"),
                    SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.FunctionsComponentsThatArePartOfThisDeployment{
                    Name:                  models.ToPointer("name4"),
                    Namespace:             models.ToPointer("namespace8"),
                    SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.FunctionsComponentsThatArePartOfThisDeployment{
                    Name:                  models.ToPointer("name4"),
                    Namespace:             models.ToPointer("namespace8"),
                    SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Id:                    models.ToPointer("id0"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        CreatedAt:               models.ToPointer(parseTime(time.RFC3339, "2020-11-19T20:27:18Z", func(err error) { log.Fatalln(err) })),
        DefaultIngress:          models.ToPointer("digitalocean.com"),
        Domains:                 []models.ContainsAllDomainsForTheApp{
            models.ContainsAllDomainsForTheApp{
                CertificateExpiresAt:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                Id:                      models.ToPointer("id0"),
                Phase:                   models.ToPointer(models.Phase1_Configuring),
                Progress:                models.ToPointer(models.Progress1{
                    Steps:                 []interface{}{
                        interface{}("[key1, val1][key2, val2]"),
                        interface{}("[key1, val1][key2, val2]"),
                        interface{}("[key1, val1][key2, val2]"),
                    },
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                RotateValidationRecords: models.ToPointer(false),
                AdditionalProperties:    map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Id:                      models.ToPointer("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf"),
        LastDeploymentCreatedAt: models.ToPointer(parseTime(time.RFC3339, "2020-11-19T20:27:18Z", func(err error) { log.Fatalln(err) })),
        LiveDomain:              models.ToPointer("live_domain"),
        LiveUrl:                 models.ToPointer("google.com"),
        LiveUrlBase:             models.ToPointer("digitalocean.com"),
        OwnerUuid:               models.ToPointer("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf"),
        ProjectId:               models.ToPointer("88b72d1a-b78a-4d9f-9090-b53c4399073f"),
        Spec:                    models.AppSpec{
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
        TierSlug:                models.ToPointer("basic"),
        UpdatedAt:               models.ToPointer(parseTime(time.RFC3339, "2020-12-01T00:42:16Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:    map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



