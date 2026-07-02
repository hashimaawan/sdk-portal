# V2 Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2RegistryRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` |
| `region` | [`Region6 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/region-6.md) | Optional | Slug of the region where registry data is stored. When not provided, a region will be selected. |
| `subscriptionTierSlug` | [`SubscriptionTierSlug`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/subscription-tier-slug.md) | Required | The slug of the subscription tier to sign up for. Valid values can be retrieved using the options endpoint. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Region6,
  SubscriptionTierSlug,
  V2RegistryRequest,
} from 'digitalocean-apilib';

const v2RegistryRequest: V2RegistryRequest = {
  name: 'example',
  subscriptionTierSlug: SubscriptionTierSlug.Basic,
  region: Region6.Fra1,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



