# V2 Reports Droplet Neighbors Ids Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBSZXBvcnRzJTI1MjBEcm9wbGV0JTI1MjBOZWlnaGJvcnMlMjUyMElkcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2ReportsDropletNeighborsIdsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `neighborIds` | `number[] \| undefined` | Optional | An array of arrays. Each array will contain a set of Droplet IDs for Droplets that share a physical server. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2ReportsDropletNeighborsIdsResponse } from 'digitalocean-apilib';

const v2ReportsDropletNeighborsIdsResponse: V2ReportsDropletNeighborsIdsResponse = {
  neighborIds: [
    168671828168663509168671815,
    168671883168671750
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



