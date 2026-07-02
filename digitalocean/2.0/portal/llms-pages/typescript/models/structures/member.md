# Member

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk1lbWJlcg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Member`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the resource was created. |
| `name` | `string \| undefined` | Optional | The name of the resource. |
| `urn` | `string \| undefined` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Member } from 'digitalocean-apilib';

const member: Member = {
  createdAt: '2020-03-13T19:30:48Z',
  name: 'nyc1-load-balancer-01',
  urn: 'do:droplet:13457723',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



