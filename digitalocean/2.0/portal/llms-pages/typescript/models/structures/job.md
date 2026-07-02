# Job

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkpvYg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Job`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `buildCommand` | `string \| undefined` | Optional | An optional build command to run while building this component from source. |
| `dockerfilePath` | `string \| undefined` | Optional | The path to the Dockerfile relative to the root of the repo. If set, it will be used to build this component. Otherwise, App Platform will attempt to build it using buildpacks. |
| `environmentSlug` | `string \| undefined` | Optional | An environment slug describing the type of this app. For a full list, please refer to [the product documentation](https://www.digitalocean.com/docs/app-platform/). |
| `envs` | [`Env[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `git` | [`Git \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/git.md) | Optional | - |
| `github` | [`Github \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/github.md) | Optional | - |
| `gitlab` | [`Gitlab \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/gitlab.md) | Optional | - |
| `image` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `logDestinations` | [`ConfigurationsForExternalLogging \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/configurations-for-external-logging.md) | Optional | - |
| `name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `runCommand` | `string \| undefined` | Optional | An optional run command to override the component's default. |
| `sourceDir` | `string \| undefined` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `instanceCount` | `bigint \| undefined` | Optional | The amount of instances that this component should be scaled to. Default: 1<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `instanceSizeSlug` | [`InstanceSizeSlug \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/instance-size-slug.md) | Optional | The instance size to use for this component. Default: `basic-xxs`<br><br>**Default**: `InstanceSizeSlug.Basicxxs` |
| `kind` | [`Kind \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/kind.md) | Optional | - UNSPECIFIED: Default job type, will auto-complete to POST_DEPLOY kind.<br>- PRE_DEPLOY: Indicates a job that runs before an app deployment.<br>- POST_DEPLOY: Indicates a job that runs after an app deployment.<br>- FAILED_DEPLOY: Indicates a job that runs after a component fails to deploy.<br><br>**Default**: `Kind.Unspecified` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  InstanceSizeSlug,
  Job,
  Kind,
  Scope,
  Type2,
} from 'digitalocean-apilib';

const job: Job = {
  name: 'api',
  buildCommand: 'npm run build',
  dockerfilePath: 'path/to/Dockerfile',
  environmentSlug: 'node-js',
  envs: [
    {
      key: 'key2',
      scope: Scope.Unset,
      type: Type2.General,
      value: 'value4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      key: 'key2',
      scope: Scope.Unset,
      type: Type2.General,
      value: 'value4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  git: {
    branch: 'branch8',
    repoCloneUrl: 'repo_clone_url8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  runCommand: 'bin/api',
  sourceDir: 'path/to/dir',
  instanceCount: BigInt(2),
  instanceSizeSlug: InstanceSizeSlug.Basicxxs,
  kind: Kind.PreDeploy,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



