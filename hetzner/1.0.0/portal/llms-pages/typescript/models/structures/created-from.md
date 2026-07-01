# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from

*This model accepts additional fields of type unknown.*


# Interface Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Server the Image was created from |
| `name` | `string` | Required | Server name at the time the Image was created |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreatedFrom } from 'hetzner-cloud-apilib';

const createdFrom: CreatedFrom = {
  id: 1,
  name: 'Server',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



