# V2 Droplets Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing information about a resource to be scheduled for deletion.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floatingIps` | `string[] \| undefined` | Optional | An array of unique identifiers for the floating IPs to be scheduled for deletion. |
| `reservedIps` | `string[] \| undefined` | Optional | An array of unique identifiers for the reserved IPs to be scheduled for deletion. |
| `snapshots` | `string[] \| undefined` | Optional | An array of unique identifiers for the snapshots to be scheduled for deletion. |
| `volumeSnapshots` | `string[] \| undefined` | Optional | An array of unique identifiers for the volume snapshots to be scheduled for deletion. |
| `volumes` | `string[] \| undefined` | Optional | An array of unique identifiers for the volumes to be scheduled for deletion. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  V2DropletsDestroyWithAssociatedResourcesSelectiveRequest,
} from 'digitalocean-apilib';

const v2DropletsDestroyWithAssociatedResourcesSelectiveRequest: V2DropletsDestroyWithAssociatedResourcesSelectiveRequest = {
  floatingIps: [
    '6186916'
  ],
  reservedIps: [
    '6186916'
  ],
  snapshots: [
    '61486916'
  ],
  volumeSnapshots: [
    'edb0478d-7436-11ea-86e6-0a58ac144b91'
  ],
  volumes: [
    'ba49449a-7435-11ea-b89e-0a58ac14480f'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



