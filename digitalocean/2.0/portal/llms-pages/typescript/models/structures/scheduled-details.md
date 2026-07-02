# Scheduled Details

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNjaGVkdWxlZERldGFpbHM

Trigger details for SCHEDULED type, where body is optional.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ScheduledDetails`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Body \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/body.md) | Optional | Optional data to be sent to function while triggering the function. |
| `cron` | `string` | Required | valid cron expression string which is required for SCHEDULED type triggers. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ScheduledDetails } from 'digitalocean-apilib';

const scheduledDetails: ScheduledDetails = {
  cron: '* * * * *',
  body: {
    name: 'name6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



