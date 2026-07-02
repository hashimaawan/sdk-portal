# Static Site

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXRpY1NpdGU

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`StaticSite`


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
| `catchallDocument` | `string \| undefined` | Optional | The name of the document to use as the fallback for any requests to documents that are not found when serving this static site. Only 1 of `catchall_document` or `error_document` can be set. |
| `cors` | [`Cors \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/cors.md) | Optional | - |
| `errorDocument` | `string \| undefined` | Optional | The name of the error document to use when serving this static site. Default: 404.html. If no such file exists within the built assets, App Platform will supply one.<br><br>**Default**: `'404.html'` |
| `indexDocument` | `string \| undefined` | Optional | The name of the index document to use when serving this static site. Default: index.html<br><br>**Default**: `'index.html'` |
| `outputDir` | `string \| undefined` | Optional | An optional path to where the built assets will be located, relative to the build context. If not set, App Platform will automatically scan for these directory names: `_static`, `dist`, `public`, `build`. |
| `routes` | [`ACriterionForRoutingHttpTrafficToAComponent[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Scope, StaticSite, Type2 } from 'digitalocean-apilib';

const staticSite: StaticSite = {
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
  catchallDocument: 'index.html',
  errorDocument: 'error.html',
  indexDocument: 'main.html',
  outputDir: 'dist/',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



