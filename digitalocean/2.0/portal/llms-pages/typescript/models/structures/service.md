# Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZpY2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Service`


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
| `cors` | [`Cors \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/cors.md) | Optional | - |
| `healthCheck` | [`HealthCheck \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/health-check.md) | Optional | - |
| `httpPort` | `bigint \| undefined` | Optional | The internal port on which this service's run command will listen. Default: 8080<br>If there is not an environment variable with the name `PORT`, one will be automatically added with its value set to the value of this field.<br><br>**Constraints**: `>= 1`, `<= 65535` |
| `internalPorts` | `bigint[] \| undefined` | Optional | The ports on which this service will listen for internal traffic. |
| `routes` | [`ACriterionForRoutingHttpTrafficToAComponent[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { InstanceSizeSlug, Scope, Service, Type2 } from 'digitalocean-apilib';

const service: Service = {
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
  httpPort: BigInt(3000),
  internalPorts: [
    BigInt(80),
    BigInt(443)
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



