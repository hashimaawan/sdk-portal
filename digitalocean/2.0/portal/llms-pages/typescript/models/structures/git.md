# Git

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkdpdA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Git`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `string \| undefined` | Optional | The name of the branch to use |
| `repoCloneUrl` | `string \| undefined` | Optional | The clone URL of the repo. Example: `https://github.com/digitalocean/sample-golang.git` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Git } from 'digitalocean-apilib';

const git: Git = {
  branch: 'main',
  repoCloneUrl: 'https://github.com/digitalocean/sample-golang.git',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



