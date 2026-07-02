# Image 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdlMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Image1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format that represents when the image was created. |
| `Description` | `*string` | Optional | An optional free-form text field to describe an image. |
| `Distribution` | [`*models.Distribution`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/distribution.md) | Optional | The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place. |
| `ErrorMessage` | `*string` | Optional | A string containing information about errors that may occur when importing<br>a custom image. |
| `Id` | `*int` | Optional, Read-only | A unique number that can be used to identify and reference a specific image. |
| `MinDiskSize` | `models.Optional[int]` | Optional | The minimum disk size in GB required for a Droplet to use this image.<br><br>**Constraints**: `>= 0` |
| `Name` | `*string` | Optional | The display name that has been given to an image.  This is what is shown in the control panel and is generally a descriptive title for the image in question. |
| `Public` | `*bool` | Optional | This is a boolean value that indicates whether the image in question is public or not. An image that is public is available to all accounts. A non-public image is only accessible from your account. |
| `Regions` | [`[]models.Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/region-2.md) | Optional | This attribute is an array of the regions that the image is available in. The regions are represented by their identifying slug values. |
| `SizeGigabytes` | `models.Optional[float64]` | Optional | The size of the image in gigabytes. |
| `Slug` | `models.Optional[string]` | Optional | A uniquely identifying string that is associated with each of the DigitalOcean-provided public images. These can be used to reference a public image as an alternative to the numeric id. |
| `Status` | [`*models.Status7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-7.md) | Optional | A status string indicating the state of a custom image. This may be `NEW`,<br>`available`, `pending`, `deleted`, or `retired`. |
| `Tags` | `models.Optional[[]string]` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `Type` | [`*models.Type9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-9.md) | Optional | Describes the kind of image. It may be one of `base`, `snapshot`, `backup`, `custom`, or `admin`. Respectively, this specifies whether an image is a DigitalOcean base OS image, user-generated Droplet snapshot, automatically created Droplet backup, user-provided virtual machine image, or an image used for DigitalOcean managed resources (e.g. DOKS worker nodes). |
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
    image1 := models.Image1{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-05-04T22:23:02Z", func(err error) { log.Fatalln(err) })),
        Description:           models.ToPointer("description2"),
        Distribution:          models.ToPointer(models.Distribution_Ubuntu),
        ErrorMessage:          models.ToPointer("error_message0"),
        Id:                    models.ToPointer(7555620),
        MinDiskSize:           models.NewOptional(models.ToPointer(20)),
        Name:                  models.ToPointer("Nifty New Snapshot"),
        Public:                models.ToPointer(true),
        Regions:               []models.Region2{
            models.Region2_Nyc1,
            models.Region2_Nyc2,
        },
        SizeGigabytes:         models.NewOptional(models.ToPointer(float64(2.34))),
        Slug:                  models.NewOptional(models.ToPointer("nifty1")),
        Status:                models.ToPointer(models.Status7_New),
        Tags:                  models.NewOptional(models.ToPointer([]string{
            "base-image",
            "prod",
        })),
        Type:                  models.ToPointer(models.Type9_Snapshot),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



