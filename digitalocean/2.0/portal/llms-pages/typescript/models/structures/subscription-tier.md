# Subscription Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvblRpZXI

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`SubscriptionTier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allowStorageOverage` | `boolean \| undefined` | Optional | A boolean indicating whether the subscription tier supports additional storage above what is included in the base plan at an additional cost per GiB used. |
| `includedBandwidthBytes` | `bigint \| undefined` | Optional | The amount of outbound data transfer included in the subscription tier in bytes. |
| `includedRepositories` | `number \| undefined` | Optional | The number of repositories included in the subscription tier. `0` indicates that the subscription tier includes unlimited repositories. |
| `includedStorageBytes` | `bigint \| undefined` | Optional | The amount of storage included in the subscription tier in bytes. |
| `monthlyPriceInCents` | `number \| undefined` | Optional | The monthly cost of the subscription tier in cents. |
| `name` | `string \| undefined` | Optional | The name of the subscription tier. |
| `slug` | `string \| undefined` | Optional | The slug identifier of the subscription tier. |
| `storageOveragePriceInCents` | `number \| undefined` | Optional | The price paid in cents per GiB for additional storage beyond what is included in the subscription plan. |
| `eligibilityReasons` | [`EligibilityReason[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/eligibility-reason.md) | Optional | If your account is not eligible to use a certain subscription tier, this will include a list of reasons that prevent you from using the tier. |
| `eligible` | `boolean \| undefined` | Optional | A boolean indicating whether your account it eligible to use a certain subscription tier. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { EligibilityReason, SubscriptionTier } from 'digitalocean-apilib';

const subscriptionTier: SubscriptionTier = {
  allowStorageOverage: true,
  includedBandwidthBytes: BigInt(5368709120),
  includedRepositories: 5,
  includedStorageBytes: BigInt(5368709120),
  monthlyPriceInCents: 500,
  name: 'Basic',
  slug: 'basic',
  storageOveragePriceInCents: 2,
  eligibilityReasons: [
    EligibilityReason.OverRepositoryLimit
  ],
  eligible: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



