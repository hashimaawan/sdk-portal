# Reserve to Region

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ReserveToRegion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string \| undefined` | Optional | The UUID of the project to which the floating IP will be assigned. |
| `region` | `string` | Required | The slug identifier for the region the floating IP will be reserved to. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ReserveToRegion } from 'digitalocean-apilib';

const reserveToRegion: ReserveToRegion = {
  region: 'nyc3',
  projectId: '746c6152-2fa2-11ed-92d3-27aaa54e4988',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



