# Resources 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc291cmNlczE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Resources1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the project was created. |
| `links` | [`Links4 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links-4.md) | Optional | The links object contains the `self` object, which contains the resource relationship. |
| `status` | [`Status14 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-14.md) | Optional | The status of assigning and fetching the resources. |
| `urn` | `string \| undefined` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Resources1, Status14 } from 'digitalocean-apilib';

const resources1: Resources1 = {
  assignedAt: '2018-09-28T19:26:37Z',
  links: {
    self: 'self2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  status: Status14.Ok,
  urn: 'do:droplet:13457723',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



