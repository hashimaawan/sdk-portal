# Kind

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRktpbmQ

- UNSPECIFIED: Default job type, will auto-complete to POST_DEPLOY kind.
- PRE_DEPLOY: Indicates a job that runs before an app deployment.
- POST_DEPLOY: Indicates a job that runs after an app deployment.
- FAILED_DEPLOY: Indicates a job that runs after a component fails to deploy.


# Class Name

`Kind`


# Fields

| Name |
|  --- |
| `Unspecified` |
| `PreDeploy` |
| `PostDeploy` |
| `FailedDeploy` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    kind := models.Kind_PostDeploy

}
```



