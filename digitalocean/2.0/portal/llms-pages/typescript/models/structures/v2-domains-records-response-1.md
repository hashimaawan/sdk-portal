# V2 Domains Records Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DomainsRecordsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domainRecord` | [`DomainRecord \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/domain-record.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DomainsRecordsResponse1 } from 'digitalocean-apilib';

const v2DomainsRecordsResponse1: V2DomainsRecordsResponse1 = {
  domainRecord: {
    type: 'A',
    data: '162.10.66.0',
    flags: null,
    id: 28448433,
    name: 'www',
    port: null,
    priority: null,
    tag: null,
    ttl: 1800,
    weight: null,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



