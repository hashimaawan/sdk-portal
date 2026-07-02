# Allow Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFsbG93T3JpZ2lu

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`AllowOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `exact` | `string \| undefined` | Optional | Exact string match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `prefix` | `string \| undefined` | Optional | Prefix-based match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `regex` | `string \| undefined` | Optional | RE2 style regex-based match. Only 1 of `exact`, `prefix`, or `regex` must be set. For more information about RE2 syntax, see: https://github.com/google/re2/wiki/Syntax<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { AllowOrigin } from 'digitalocean-apilib';

const allowOrigin: AllowOrigin = {
  exact: 'https://www.example.com',
  prefix: 'https://www.example.com',
  regex: '^.*example.com',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



