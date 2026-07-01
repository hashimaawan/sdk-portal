# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from


# Interface Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Server the Image was created from |
| `name` | `string` | Required | Server name at the time the Image was created |


# Example

```ts
import { CreatedFrom } from 'hetzner-cloud-apilib';

const createdFrom: CreatedFrom = {
  id: 1,
  name: 'Server',
};
```



