# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ


# Interface Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | [`Tag[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/tag.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { ListTagsForResourceOutput } from 'amazon-athenalib';

const listTagsForResourceOutput: ListTagsForResourceOutput = {
  tags: [
    {
      key: 'Key0',
      value: 'Value6',
    },
    {
      key: 'Key0',
      value: 'Value6',
    },
    {
      key: 'Key0',
      value: 'Value6',
    }
  ],
  nextToken: 'NextToken4',
};
```



