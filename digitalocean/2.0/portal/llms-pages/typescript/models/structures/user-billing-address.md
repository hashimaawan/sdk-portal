# User Billing Address

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlVzZXJCaWxsaW5nQWRkcmVzcw

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`UserBillingAddress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addressLine1` | `string \| undefined` | Optional | Street address line 1 |
| `addressLine2` | `string \| undefined` | Optional | Street address line 2 |
| `city` | `string \| undefined` | Optional | City |
| `countryIso2Code` | `string \| undefined` | Optional | Country (ISO2) code |
| `createdAt` | `string \| undefined` | Optional | Timestamp billing address was created |
| `postalCode` | `string \| undefined` | Optional | Postal code |
| `region` | `string \| undefined` | Optional | Region |
| `updatedAt` | `string \| undefined` | Optional | Timestamp billing address was updated |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { UserBillingAddress } from 'digitalocean-apilib';

const userBillingAddress: UserBillingAddress = {
  addressLine1: '101 Shark Row',
  addressLine2: 'address_line24',
  city: 'Atlantis',
  countryIso2Code: 'US',
  createdAt: '2019-09-03T16:34:46.000+00:00',
  postalCode: '12345',
  region: 'OC',
  updatedAt: '2019-09-03T16:34:46.000+00:00',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



