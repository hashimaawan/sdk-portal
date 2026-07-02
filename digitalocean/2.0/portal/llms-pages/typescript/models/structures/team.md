# Team

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlRlYW0

When authorized in a team context, includes information about the current team.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Team`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | The name for the current team. |
| `uuid` | `string \| undefined` | Optional | The unique universal identifier for the current team. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Team } from 'digitalocean-apilib';

const team: Team = {
  name: 'My Team',
  uuid: '5df3e3004a17e242b7c20ca6c9fc25b701a47ece',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



