# Subscription Tier Slug

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvblRpZXJTbHVn

The slug of the subscription tier to sign up for. Valid values can be retrieved using the options endpoint.


# Class Name

`SubscriptionTierSlug`


# Fields

| Name |
|  --- |
| `Starter` |
| `Basic` |
| `Professional` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    subscriptionTierSlug := models.SubscriptionTierSlug_Professional

}
```



