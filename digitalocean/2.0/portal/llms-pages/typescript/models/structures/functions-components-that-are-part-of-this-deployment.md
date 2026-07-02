# Functions Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkZ1bmN0aW9ucyUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`FunctionsComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | - |
| `namespace` | `string \| undefined` | Optional | The namespace where the functions are deployed. |
| `sourceCommitHash` | `string \| undefined` | Optional | The commit hash of the repository that was used to build this functions component. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  FunctionsComponentsThatArePartOfThisDeployment,
} from 'digitalocean-apilib';

const functionsComponentsThatArePartOfThisDeployment: FunctionsComponentsThatArePartOfThisDeployment = {
  name: 'my-functions-component',
  namespace: 'ap-b2a93513-8d9b-4223-9d61-5e7272c81c32',
  sourceCommitHash: '54d4a727f457231062439895000d45437c7bb405',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



