# Account

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFjY291bnQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Account`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletLimit` | `number` | Required | The total number of Droplets current user or team may have active at one time. |
| `email` | `string` | Required | The email address used by the current user to register for DigitalOcean. |
| `emailVerified` | `boolean` | Required | If true, the user has verified their account via email. False otherwise.<br><br>**Default**: `false` |
| `floatingIpLimit` | `number` | Required | The total number of Floating IPs the current user or team may have. |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status.md) | Required | This value is one of "active", "warning" or "locked".<br><br>**Default**: `Status.Active` |
| `statusMessage` | `string` | Required | A human-readable message giving more details about the status of the account. |
| `team` | [`Team \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/team.md) | Optional | When authorized in a team context, includes information about the current team. |
| `uuid` | `string` | Required | The unique universal identifier for the current user. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Account, Status } from 'digitalocean-apilib';

const account: Account = {
  dropletLimit: 25,
  email: 'sammy@digitalocean.com',
  emailVerified: true,
  floatingIpLimit: 5,
  status: Status.Active,
  statusMessage: ' ',
  uuid: 'b6fr89dbf6d9156cace5f3c78dc9851d957381ef',
  team: {
    name: 'name0',
    uuid: 'uuid6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



