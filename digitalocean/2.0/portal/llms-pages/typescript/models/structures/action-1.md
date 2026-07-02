# Action 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFjdGlvbjE

The linked actions can be used to check the status of a Droplet's create event.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Action1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string \| undefined` | Optional | A URL that can be used to access the action. |
| `id` | `number \| undefined` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `rel` | `string \| undefined` | Optional | A string specifying the type of the related action. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Action1 } from 'digitalocean-apilib';

const action1: Action1 = {
  href: 'https://api.digitalocean.com/v2/actions/7515',
  id: 7515,
  rel: 'create',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



