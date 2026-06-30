# File

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkZpbGU

*This model accepts additional fields of type interface{}.*


# Class Name

`File`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Content` | `*string` | Optional | Base64-encoded contents of the file. Only set if size <= OP_MAX_INLINE_FILE_SIZE_KB kb and `inline_files` is set to `true`. |
| `ContentPath` | `*string` | Optional, Read-only | Path of the Connect API that can be used to download the contents of this file. |
| `Id` | `*string` | Optional | ID of the file |
| `Name` | `*string` | Optional | Name of the file |
| `Section` | [`*models.Section1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/section-1.md) | Optional | For files that are in a section, this field describes the section. |
| `Size` | `*int` | Optional | Size in bytes of the file |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    file := models.File{
        Content:               models.ToPointer("VGhlIGZ1dHVyZSBiZWxvbmdzIHRvIHRoZSBjdXJpb3VzLgo="),
        ContentPath:           models.ToPointer("v1/vaults/ionaiwtdvgclrixbt6ztpqcxnq/items/p7eflcy7f5mk7vg6zrzf5rjjyu/files/6r65pjq33banznomn7q22sj44e/content"),
        Id:                    models.ToPointer("6r65pjq33banznomn7q22sj44e"),
        Name:                  models.ToPointer("foo.txt"),
        Section:               models.ToPointer(models.Section1{
            Id:                    models.ToPointer("id6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Size:                  models.ToPointer(35),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



