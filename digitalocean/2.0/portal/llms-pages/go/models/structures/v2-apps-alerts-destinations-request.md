# V2 Apps Alerts Destinations Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Emails` | `[]string` | Optional | - |
| `SlackWebhooks` | [`[]models.SlackWebhooksToSendAlertsTo`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2AppsAlertsDestinationsRequest := models.V2AppsAlertsDestinationsRequest{
        Emails:                []string{
            "sammy@digitalocean.com",
        },
        SlackWebhooks:         []models.SlackWebhooksToSendAlertsTo{
            models.SlackWebhooksToSendAlertsTo{
                Channel:               models.ToPointer("channel8"),
                Url:                   models.ToPointer("url0"),
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



