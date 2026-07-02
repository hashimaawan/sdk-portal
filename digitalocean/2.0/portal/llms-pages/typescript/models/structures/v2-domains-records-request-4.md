# V2 Domains Records Request 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXF1ZXN0NA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DomainsRecordsRequest4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `string` | Required | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `flags` | `number \| null \| undefined` | Optional | An unsigned integer between 0-255 used for CAA records. |
| `id` | `number \| undefined` | Optional, Read-only | A unique identifier for each domain record. |
| `name` | `string \| undefined` | Optional | The host name, alias, or service being defined by the record. |
| `port` | `number \| null \| undefined` | Optional | The port for SRV records. |
| `priority` | `number \| null` | Required | The priority for SRV and MX records. |
| `tag` | `string \| null \| undefined` | Optional | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `ttl` | `number \| undefined` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `type` | `string` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `weight` | `number \| null \| undefined` | Optional | The weight for SRV records. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DomainsRecordsRequest4 } from 'digitalocean-apilib';

const v2DomainsRecordsRequest4: V2DomainsRecordsRequest4 = {
  data: 'ns1.digitalocean.com',
  priority: null,
  type: 'NS',
  flags: 172,
  id: 28448429,
  name: '@',
  port: 48,
  tag: 'tag6',
  ttl: 1800,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



