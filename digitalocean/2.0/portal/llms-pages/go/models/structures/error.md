# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkVycm9y

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Code` | [`*models.Code`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/code.md) | Optional | A code identifier that represents the failing condition.<br><br>Failing conditions:<br><br>- `incompatible_phase` - indicates that the deployment's phase is not suitable for rollback.<br>- `incompatible_result` - indicates that the deployment's result is not suitable for rollback.<br>- `exceeded_revision_limit` - indicates that the app has exceeded the rollback revision limits for its tier.<br>- `app_pinned` - indicates that there is already a rollback in progress and the app is pinned.<br>- `database_config_conflict` - indicates that the deployment's database config is different than the current config.<br>- `region_conflict` - indicates that the deployment's region differs from the current app region.<br><br>Warning conditions:<br><br>- `static_site_requires_rebuild` - indicates that the deployment contains at least one static site that will require a rebuild.<br>- `image_source_missing_digest` - indicates that the deployment contains at least one component with an image source that is missing a digest. |
| `Components` | `[]string` | Optional | - |
| `Message` | `*string` | Optional | A human-readable message describing the failing condition. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    mError := models.Error{
        Code:                  models.ToPointer(models.Code_ExceededRevisionLimit),
        Components:            []string{
            "www",
        },
        Message:               models.ToPointer("the deployment is past the maximum historical revision limit of 0 for the \"starter\" app tier"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



