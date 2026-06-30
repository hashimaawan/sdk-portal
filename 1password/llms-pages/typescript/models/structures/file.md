# File

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkZpbGU

*This model accepts additional fields of type unknown.*


# Interface Name

`File`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `string \| undefined` | Optional | Base64-encoded contents of the file. Only set if size <= OP_MAX_INLINE_FILE_SIZE_KB kb and `inline_files` is set to `true`. |
| `contentPath` | `string \| undefined` | Optional, Read-only | Path of the Connect API that can be used to download the contents of this file. |
| `id` | `string \| undefined` | Optional | ID of the file |
| `name` | `string \| undefined` | Optional | Name of the file |
| `section` | [`Section1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/section-1.md) | Optional | For files that are in a section, this field describes the section. |
| `size` | `number \| undefined` | Optional | Size in bytes of the file |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { File } from 'm-1-password-connectlib';

const file: File = {
  content: 'VGhlIGZ1dHVyZSBiZWxvbmdzIHRvIHRoZSBjdXJpb3VzLgo=',
  contentPath: 'v1/vaults/ionaiwtdvgclrixbt6ztpqcxnq/items/p7eflcy7f5mk7vg6zrzf5rjjyu/files/6r65pjq33banznomn7q22sj44e/content',
  id: '6r65pjq33banznomn7q22sj44e',
  name: 'foo.txt',
  section: {
    id: 'id6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  size: 35,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



