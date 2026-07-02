# V2 Cdn Endpoints Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CdnEndpointsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endpoint` | [`Endpoint \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/endpoint.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2CdnEndpointsResponse1 } from 'digitalocean-apilib';

const v2CdnEndpointsResponse1: V2CdnEndpointsResponse1 = {
  endpoint: {
    origin: 'origin2',
    certificateId: '00001b94-0000-0000-0000-000000000000',
    createdAt: '2016-03-13T12:52:32.123Z',
    customDomain: 'custom_domain6',
    endpoint: 'endpoint6',
    id: '00001f7a-0000-0000-0000-000000000000',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



