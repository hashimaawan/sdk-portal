# Git

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkdpdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Git`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Branch` | `*string` | Optional | The name of the branch to use |
| `RepoCloneUrl` | `*string` | Optional | The clone URL of the repo. Example: `https://github.com/digitalocean/sample-golang.git` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    git := models.Git{
        Branch:                models.ToPointer("main"),
        RepoCloneUrl:          models.ToPointer("https://github.com/digitalocean/sample-golang.git"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



