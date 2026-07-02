# V2 Cdn Endpoints Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CdnEndpointsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endpoints` | [`Endpoint[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/endpoint.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Ttl, V2CdnEndpointsResponse } from 'digitalocean-apilib';

const v2CdnEndpointsResponse: V2CdnEndpointsResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  endpoints: [
    {
      origin: 'static-images.nyc3.digitaloceanspaces.com',
      certificateId: '892071a0-bb95-49bc-8021-3afd67a210bf',
      createdAt: '2018-07-19T15:04:16Z',
      customDomain: 'static.example.com',
      endpoint: 'static-images.nyc3.cdn.digitaloceanspaces.com',
      id: '19f06b6a-3ace-4315-b086-499a0e521b76',
      ttl: Ttl.Enum3600,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'last6',
      next: 'next2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



