# Papertrail

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlBhcGVydHJhaWw

Papertrail configuration.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Papertrail`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endpoint` | `string` | Required | Papertrail syslog endpoint. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Papertrail } from 'digitalocean-apilib';

const papertrail: Papertrail = {
  endpoint: 'https://mypapertrailendpoint.com',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



