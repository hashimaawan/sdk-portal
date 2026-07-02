# Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkVuZHBvaW50

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Endpoint`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificateId` | `string \| undefined` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the CDN endpoint was created. |
| `customDomain` | `string \| undefined` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `endpoint` | `string \| undefined` | Optional, Read-only | The fully qualified domain name (FQDN) from which the CDN-backed content is served. |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a CDN endpoint. |
| `origin` | `string` | Required | The fully qualified domain name (FQDN) for the origin server which provides the content for the CDN. This is currently restricted to a Space. |
| `ttl` | [`Ttl \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl.Enum3600` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Endpoint, Ttl } from 'digitalocean-apilib';

const endpoint: Endpoint = {
  origin: 'static-images.nyc3.digitaloceanspaces.com',
  certificateId: '892071a0-bb95-49bc-8021-3afd67a210bf',
  createdAt: '2018-03-21T16:02:37Z',
  customDomain: 'static.example.com',
  endpoint: 'static-images.nyc3.cdn.digitaloceanspaces.com',
  id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  ttl: Ttl.Enum3600,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



