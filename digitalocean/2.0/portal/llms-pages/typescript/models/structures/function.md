# Function

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkZ1bmN0aW9u

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Function`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alerts` | [`Alert[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/alert.md) | Optional | - |
| `cors` | [`Cors \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/cors.md) | Optional | - |
| `envs` | [`Env[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `git` | [`Git \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/git.md) | Optional | - |
| `github` | [`Github \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/github.md) | Optional | - |
| `gitlab` | [`Gitlab \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/gitlab.md) | Optional | - |
| `logDestinations` | [`ConfigurationsForExternalLogging \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/configurations-for-external-logging.md) | Optional | - |
| `name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `routes` | [`ACriterionForRoutingHttpTrafficToAComponent[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `sourceDir` | `string \| undefined` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Function,
  Operator,
  Rule,
  Scope,
  Type2,
  Window,
} from 'digitalocean-apilib';

const mFunction: Function = {
  name: 'api',
  alerts: [
    {
      disabled: false,
      operator: Operator.LessThan,
      rule: Rule.MemUtilization,
      value: 12.58,
      window: Window.ThirtyMinutes,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  cors: {
    allowCredentials: false,
    allowHeaders: [
      'allow_headers9',
      'allow_headers0'
    ],
    allowMethods: [
      'allow_methods8',
      'allow_methods9',
      'allow_methods0'
    ],
    allowOrigins: [
      {}
    ],
    exposeHeaders: [
      'expose_headers2'
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
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
  github: {
    branch: 'branch4',
    deployOnPush: false,
    repo: 'repo6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  sourceDir: 'path/to/dir',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



