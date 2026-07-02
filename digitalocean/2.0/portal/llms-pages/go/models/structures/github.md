# Github

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkdpdGh1Yg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Github`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Branch` | `*string` | Optional | The name of the branch to use |
| `DeployOnPush` | `*bool` | Optional | Whether to automatically deploy new commits made to the repo |
| `Repo` | `*string` | Optional | The name of the repo in the format owner/repo. Example: `digitalocean/sample-golang` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    github := models.Github{
        Branch:                models.ToPointer("main"),
        DeployOnPush:          models.ToPointer(true),
        Repo:                  models.ToPointer("digitalocean/sample-golang"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



