# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tags` | [`Tag[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/tag.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { TagResourceInput } from 'amazon-athenalib';

const tagResourceInput: TagResourceInput = {
  resourceArn: 'ResourceARN6',
  tags: [
    {
      key: 'Key0',
      value: 'Value6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



