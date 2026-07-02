# V2 Firewalls Tags Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFRhZ3MlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FirewallsTagsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | `string[] \| null` | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FirewallsTagsRequest } from 'digitalocean-apilib';

const v2FirewallsTagsRequest: V2FirewallsTagsRequest = {
  tags: [
    'tags1'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



