# File

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkZpbGU

*This model accepts additional fields of type object.*


# Class Name

`File`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Content` | `string` | Optional | Base64-encoded contents of the file. Only set if size <= OP_MAX_INLINE_FILE_SIZE_KB kb and `inline_files` is set to `true`. |
| `ContentPath` | `string` | Optional, Read-only | Path of the Connect API that can be used to download the contents of this file. |
| `Id` | `string` | Optional | ID of the file |
| `Name` | `string` | Optional | Name of the file |
| `Section` | [`Section1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/section-1.md) | Optional | For files that are in a section, this field describes the section. |
| `Size` | `int?` | Optional | Size in bytes of the file |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Http.Client;
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;
using System.IO;

File file = new File
{
    Content = "VGhlIGZ1dHVyZSBiZWxvbmdzIHRvIHRoZSBjdXJpb3VzLgo=",
    ContentPath = "v1/vaults/ionaiwtdvgclrixbt6ztpqcxnq/items/p7eflcy7f5mk7vg6zrzf5rjjyu/files/6r65pjq33banznomn7q22sj44e/content",
    Id = "6r65pjq33banznomn7q22sj44e",
    Name = "foo.txt",
    Section = new Section1
    {
        Id = "id6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Size = 35,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



