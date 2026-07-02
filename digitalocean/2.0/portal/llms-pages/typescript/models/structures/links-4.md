# Links 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpbmtzNA

The links object contains the `self` object, which contains the resource relationship.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Links4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `self` | `string \| undefined` | Optional | A URI that can be used to retrieve the resource. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Links4 } from 'digitalocean-apilib';

const links4: Links4 = {
  self: 'https://api.digitalocean.com/v2/droplets/13457723',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



