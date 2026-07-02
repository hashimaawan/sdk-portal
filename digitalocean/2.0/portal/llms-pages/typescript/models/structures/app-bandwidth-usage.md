# App Bandwidth Usage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcEJhbmR3aWR0aFVzYWdl

Bandwidth usage for an app.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`AppBandwidthUsage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string \| undefined` | Optional | The ID of the app. |
| `bandwidthBytes` | `string \| undefined` | Optional | The used bandwidth amount in bytes. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { AppBandwidthUsage } from 'digitalocean-apilib';

const appBandwidthUsage: AppBandwidthUsage = {
  appId: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  bandwidthBytes: '513668',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



