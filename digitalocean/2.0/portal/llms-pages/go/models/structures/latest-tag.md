# Latest Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxhdGVzdFRhZw

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`LatestTag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompressedSizeBytes` | `*int` | Optional | The compressed size of the tag in bytes. |
| `ManifestDigest` | `*string` | Optional | The digest of the manifest associated with the tag. |
| `RegistryName` | `*string` | Optional | The name of the container registry. |
| `Repository` | `*string` | Optional | The name of the repository. |
| `SizeBytes` | `*int` | Optional | The uncompressed size of the tag in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `Tag` | `*string` | Optional | The name of the tag. |
| `UpdatedAt` | `*time.Time` | Optional | The time the tag was last updated. |
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
    latestTag := models.LatestTag{
        CompressedSizeBytes:   models.ToPointer(2803255),
        ManifestDigest:        models.ToPointer("sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221"),
        RegistryName:          models.ToPointer("example"),
        Repository:            models.ToPointer("repo-1"),
        SizeBytes:             models.ToPointer(5861888),
        Tag:                   models.ToPointer("latest"),
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-04-09T23:54:25Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



