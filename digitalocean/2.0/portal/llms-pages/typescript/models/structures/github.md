# Github

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkdpdGh1Yg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Github`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `string \| undefined` | Optional | The name of the branch to use |
| `deployOnPush` | `boolean \| undefined` | Optional | Whether to automatically deploy new commits made to the repo |
| `repo` | `string \| undefined` | Optional | The name of the repo in the format owner/repo. Example: `digitalocean/sample-golang` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Github } from 'digitalocean-apilib';

const github: Github = {
  branch: 'main',
  deployOnPush: true,
  repo: 'digitalocean/sample-golang',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



