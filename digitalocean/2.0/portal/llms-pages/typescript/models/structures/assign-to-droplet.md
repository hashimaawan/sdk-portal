# Assign to Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwdG8lMjUyMERyb3BsZXQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`AssignToDroplet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `number` | Required | The ID of the Droplet that the floating IP will be assigned to. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { AssignToDroplet } from 'digitalocean-apilib';

const assignToDroplet: AssignToDroplet = {
  dropletId: 2457247,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



