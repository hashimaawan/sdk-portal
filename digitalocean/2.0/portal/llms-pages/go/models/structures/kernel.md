# Kernel

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRktlcm5lbA

**Note**: All Droplets created after March 2017 use internal kernels by default.
These Droplets will have this attribute set to `null`.

The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)
for Droplets with externally managed kernels. This will initially be set to
the kernel of the base image when the Droplet is created.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Kernel`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `*int` | Optional | A unique number used to identify and reference a specific kernel. |
| `Name` | `*string` | Optional | The display name of the kernel. This is shown in the web UI and is generally a descriptive title for the kernel in question. |
| `Version` | `*string` | Optional | A standard kernel version string representing the version, patch, and release information. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    kernel := models.Kernel{
        Id:                    models.ToPointer(7515),
        Name:                  models.ToPointer("DigitalOcean GrubLoader v0.2 (20160714)"),
        Version:               models.ToPointer("2016.07.13-DigitalOcean_loader_Ubuntu"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



