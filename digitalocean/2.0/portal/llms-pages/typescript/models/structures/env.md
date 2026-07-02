# Env

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkVudg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Env`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `string` | Required | The variable name<br><br>**Constraints**: *Pattern*: `^[_A-Za-z][_A-Za-z0-9]*$` |
| `scope` | [`Scope \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/scope.md) | Optional | - RUN_TIME: Made available only at run-time<br>- BUILD_TIME: Made available only at build-time<br>- RUN_AND_BUILD_TIME: Made available at both build and run-time<br><br>**Default**: `Scope.RunAndBuildTime` |
| `type` | [`Type2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-2.md) | Optional | - GENERAL: A plain-text environment variable<br>- SECRET: A secret encrypted environment variable<br><br>**Default**: `Type2.General` |
| `value` | `string \| undefined` | Optional | The value. If the type is `SECRET`, the value will be encrypted on first submission. On following submissions, the encrypted value should be used. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Env, Scope, Type2 } from 'digitalocean-apilib';

const env: Env = {
  key: 'BASE_URL',
  scope: Scope.BuildTime,
  type: Type2.General,
  value: 'http://example.com',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



