# V2 Cdn Endpoints Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CdnEndpointsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificateId` | `string \| undefined` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `customDomain` | `string \| undefined` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `ttl` | [`Ttl \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl.Enum3600` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Ttl, V2CdnEndpointsRequest } from 'digitalocean-apilib';

const v2CdnEndpointsRequest: V2CdnEndpointsRequest = {
  certificateId: '892071a0-bb95-49bc-8021-3afd67a210bf',
  customDomain: 'static.example.com',
  ttl: Ttl.Enum3600,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



