# V2 Cdn Endpoints Cache Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwQ2FjaGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CdnEndpointsCacheRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `files` | `string[]` | Required | An array of strings containing the path to the content to be purged from the CDN cache. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2CdnEndpointsCacheRequest } from 'digitalocean-apilib';

const v2CdnEndpointsCacheRequest: V2CdnEndpointsCacheRequest = {
  files: [
    'path/to/image.png',
    'path/to/css/*'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



