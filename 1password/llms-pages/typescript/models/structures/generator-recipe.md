# Generator Recipe

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkdlbmVyYXRvclJlY2lwZQ

The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value

*This model accepts additional fields of type unknown.*


# Interface Name

`GeneratorRecipe`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `characterSets` | [`CharacterSet[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/character-set.md) | Optional | **Constraints**: *Unique Items Required* |
| `excludeCharacters` | `string \| undefined` | Optional | List of all characters that should be excluded from generated passwords. |
| `length` | `number \| undefined` | Optional | Length of the generated value<br><br>**Default**: `32`<br><br>**Constraints**: `>= 1`, `<= 64` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CharacterSet, GeneratorRecipe } from 'm-1-password-connectlib';

const generatorRecipe: GeneratorRecipe = {
  characterSets: [
    CharacterSet.Letters,
    CharacterSet.Digits,
    CharacterSet.Symbols
  ],
  excludeCharacters: 'abc1',
  length: 32,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



