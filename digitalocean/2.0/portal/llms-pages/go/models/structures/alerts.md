# Alerts

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFsZXJ0cw

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Alerts`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Email` | `[]string` | Required | An email to notify on an alert trigger. |
| `Slack` | [`[]models.Slack`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/slack.md) | Required | Slack integration details. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    alerts := models.Alerts{
        Email:                 []string{
            "bob@exmaple.com",
        },
        Slack:                 []models.Slack{
            models.Slack{
                Channel:               "Production Alerts",
                Url:                   "https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



