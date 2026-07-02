# Domain

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRvbWFpbg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Domain`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Domain` | `string` | Required | The hostname for the domain<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `253`, *Pattern*: `^((xn--)?[a-zA-Z0-9]+(-[a-zA-Z0-9]+)*\.)+[a-zA-Z]{2,}\.?$` |
| `MinimumTlsVersion` | [`*models.MinimumTlsVersion`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/minimum-tls-version.md) | Optional | The minimum version of TLS a client application can use to access resources for the domain.  Must be one of the following values wrapped within quotations: `"1.2"` or `"1.3"`.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` |
| `Type` | [`*models.Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-1.md) | Optional | - DEFAULT: The default `.ondigitalocean.app` domain assigned to this app<br>- PRIMARY: The primary domain for this app that is displayed as the default in the control panel, used in bindable environment variables, and any other places that reference an app's live URL. Only one domain may be set as primary.<br>- ALIAS: A non-primary domain<br><br>**Default**: `"UNSPECIFIED"` |
| `Wildcard` | `*bool` | Optional | Indicates whether the domain includes all sub-domains, in addition to the given domain |
| `Zone` | `*string` | Optional | Optional. If the domain uses DigitalOcean DNS and you would like App<br>Platform to automatically manage it for you, set this to the name of the<br>domain on your account.<br><br>For example, If the domain you are adding is `app.domain.com`, the zone<br>could be `domain.com`. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    domain := models.Domain{
        Domain:                "app.example.com",
        MinimumTlsVersion:     models.ToPointer(models.MinimumTlsVersion_Enum13),
        Type:                  models.ToPointer(models.Type1_Default),
        Wildcard:              models.ToPointer(true),
        Zone:                  models.ToPointer("example.com"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



