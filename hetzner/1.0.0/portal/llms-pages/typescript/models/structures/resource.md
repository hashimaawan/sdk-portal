# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type unknown.*


# Interface Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Resource |
| `type` | `string` | Required | Type of resource referenced |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Resource } from 'hetzner-cloud-apilib';

const resource: Resource = {
  id: 42,
  type: 'server',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



