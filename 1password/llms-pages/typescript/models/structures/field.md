# Field

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkZpZWxk

*This model accepts additional fields of type unknown.*


# Interface Name

`Field`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entropy` | `number \| undefined` | Optional, Read-only | For fields with a purpose of `PASSWORD` this is the entropy of the value |
| `generate` | `boolean \| undefined` | Optional | If value is not present then a new value should be generated for this field<br><br>**Default**: `false` |
| `id` | `string` | Required | - |
| `label` | `string \| undefined` | Optional | - |
| `purpose` | [`Purpose \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/purpose.md) | Optional | Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types. |
| `recipe` | [`GeneratorRecipe \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/generator-recipe.md) | Optional | The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value |
| `section` | [`Section \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/section.md) | Optional | - |
| `type` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/type-1.md) | Required | **Default**: `Type1.String` |
| `value` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CharacterSet, Field, Purpose, Type1 } from 'm-1-password-connectlib';

const field: Field = {
  id: 'id6',
  type: Type1.String,
  entropy: 80.94,
  generate: false,
  label: 'label6',
  purpose: Purpose.Notes,
  recipe: {
    characterSets: [
      CharacterSet.Letters,
      CharacterSet.Symbols,
      CharacterSet.Digits
    ],
    excludeCharacters: 'excludeCharacters0',
    length: 64,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



