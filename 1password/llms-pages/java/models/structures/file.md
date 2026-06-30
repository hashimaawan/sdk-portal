# File

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkZpbGU

*This model accepts additional fields of type Object.*


# Class Name

`File`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Content` | `String` | Optional | Base64-encoded contents of the file. Only set if size <= OP_MAX_INLINE_FILE_SIZE_KB kb and `inline_files` is set to `true`. | String getContent() | setContent(String content) |
| `ContentPath` | `String` | Optional, Read-only | Path of the Connect API that can be used to download the contents of this file. | String getContentPath() | setContentPath(String contentPath) |
| `Id` | `String` | Optional | ID of the file | String getId() | setId(String id) |
| `Name` | `String` | Optional | Name of the file | String getName() | setName(String name) |
| `Section` | [`Section1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/section-1.md) | Optional | For files that are in a section, this field describes the section. | Section1 getSection() | setSection(Section1 section) |
| `Size` | `Integer` | Optional | Size in bytes of the file | Integer getSize() | setSize(Integer size) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.models.File;
import local.m1password.models.Section1;

File file = new File.Builder()
    .content("VGhlIGZ1dHVyZSBiZWxvbmdzIHRvIHRoZSBjdXJpb3VzLgo=")
    .contentPath("v1/vaults/ionaiwtdvgclrixbt6ztpqcxnq/items/p7eflcy7f5mk7vg6zrzf5rjjyu/files/6r65pjq33banznomn7q22sj44e/content")
    .id("6r65pjq33banznomn7q22sj44e")
    .name("foo.txt")
    .section(new Section1.Builder()
        .id("id6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .size(35)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



