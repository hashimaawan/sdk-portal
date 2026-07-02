# Rule 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJ1bGUx

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Rule1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterUuid` | `string \| undefined` | Optional | A unique ID for the database cluster to which the rule is applied.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall rule was created. |
| `type` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-7.md) | Required | The type of resource that the firewall rule allows to access the database cluster. |
| `uuid` | `string \| undefined` | Optional | A unique ID for the firewall rule itself.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `value` | `string` | Required | The ID of the specific resource, the name of a tag applied to a group of resources, or the IP address that the firewall rule allows to access the database cluster. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Rule1, Type7 } from 'digitalocean-apilib';

const rule1: Rule1 = {
  type: Type7.Droplet,
  value: 'ff2a6c52-5a44-4b63-b99c-0e98e7a63d61',
  clusterUuid: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
  createdAt: '2019-01-11T18:37:36Z',
  uuid: '79f26d28-ea8a-41f2-8ad8-8cfcdd020095',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



