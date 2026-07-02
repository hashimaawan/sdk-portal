# Reserve to Region 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24x

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ReserveToRegion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string \| undefined` | Optional | The UUID of the project to which the reserved IP will be assigned. |
| `region` | `string` | Required | The slug identifier for the region the reserved IP will be reserved to. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ReserveToRegion1 } from 'digitalocean-apilib';

const reserveToRegion1: ReserveToRegion1 = {
  region: 'nyc3',
  projectId: '746c6152-2fa2-11ed-92d3-27aaa54e4988',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



