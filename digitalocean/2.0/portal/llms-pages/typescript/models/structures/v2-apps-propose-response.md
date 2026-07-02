# V2 Apps Propose Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBQcm9wb3NlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsProposeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appCost` | `number \| undefined` | Optional | The monthly cost of the proposed app in USD using the next pricing plan tier. For example, if you propose an app that uses the Basic tier, the `app_tier_upgrade_cost` field displays the monthly cost of the app if it were to use the Professional tier. If the proposed app already uses the most expensive tier, the field is empty. |
| `appIsStatic` | `boolean \| undefined` | Optional | Indicates whether the app is a static app. |
| `appNameAvailable` | `boolean \| undefined` | Optional | Indicates whether the app name is available. |
| `appNameSuggestion` | `string \| undefined` | Optional | The suggested name if the proposed app name is unavailable. |
| `appTierDowngradeCost` | `number \| undefined` | Optional | The monthly cost of the proposed app in USD using the previous pricing plan tier. For example, if you propose an app that uses the Professional tier, the `app_tier_downgrade_cost` field displays the monthly cost of the app if it were to use the Basic tier. If the proposed app already uses the lest expensive tier, the field is empty. |
| `existingStaticApps` | `string \| undefined` | Optional | The maximum number of free static apps the account can have. We will charge you for any additional static apps. |
| `spec` | [`AppSpec \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsProposeResponse } from 'digitalocean-apilib';

const v2AppsProposeResponse: V2AppsProposeResponse = {
  appCost: 5,
  appIsStatic: true,
  appNameAvailable: true,
  appNameSuggestion: 'newName',
  appTierDowngradeCost: 17,
  existingStaticApps: '2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



