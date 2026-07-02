# Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoZWNr

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Check`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference the check. |
| `enabled` | `boolean \| undefined` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `true` |
| `name` | `string \| undefined` | Optional | A human-friendly display name. |
| `regions` | [`Region8[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. |
| `target` | `string \| undefined` | Optional | The endpoint to perform healthchecks on. |
| `type` | [`Type19 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-19.md) | Optional | The type of health check to perform. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Check, Region8, Type19 } from 'digitalocean-apilib';

const check: Check = {
  id: '5a4981aa-9653-4bd1-bef5-d6bff52042e4',
  enabled: true,
  name: 'Landing page check',
  regions: [
    Region8.UsEast,
    Region8.EuWest
  ],
  target: 'https://www.landingpage.com',
  type: Type19.Https,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



