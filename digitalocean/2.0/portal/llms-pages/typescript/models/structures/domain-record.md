# Domain Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRvbWFpblJlY29yZA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`DomainRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `string \| undefined` | Optional | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `flags` | `number \| null \| undefined` | Optional | An unsigned integer between 0-255 used for CAA records. |
| `id` | `number \| undefined` | Optional, Read-only | A unique identifier for each domain record. |
| `name` | `string \| undefined` | Optional | The host name, alias, or service being defined by the record. |
| `port` | `number \| null \| undefined` | Optional | The port for SRV records. |
| `priority` | `number \| null \| undefined` | Optional | The priority for SRV and MX records. |
| `tag` | `string \| null \| undefined` | Optional | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `ttl` | `number \| undefined` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `type` | `string` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `weight` | `number \| null \| undefined` | Optional | The weight for SRV records. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { DomainRecord } from 'digitalocean-apilib';

const domainRecord: DomainRecord = {
  type: 'NS',
  data: 'ns1.digitalocean.com',
  flags: 32,
  id: 28448429,
  name: '@',
  port: 164,
  ttl: 1800,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



