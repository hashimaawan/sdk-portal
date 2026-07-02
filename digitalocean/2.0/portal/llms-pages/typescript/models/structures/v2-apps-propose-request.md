# V2 Apps Propose Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBQcm9wb3NlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsProposeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string \| undefined` | Optional | An optional ID of an existing app. If set, the spec will be treated as a proposed update to the specified app. The existing app is not modified using this method. |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Engine,
  MinimumTlsVersion,
  Operator,
  Region1,
  Rule,
  Scope,
  Type1,
  Type2,
  V2AppsProposeRequest,
  Window,
} from 'digitalocean-apilib';

const v2AppsProposeRequest: V2AppsProposeRequest = {
  spec: {
    name: 'web-app-01',
    databases: [
      {
        name: 'name6',
        clusterName: 'cluster_name8',
        dbName: 'db_name0',
        dbUser: 'db_user8',
        engine: Engine.Pg,
        production: false,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    domains: [
      {
        domain: 'domain6',
        minimumTlsVersion: MinimumTlsVersion.Enum12,
        type: Type1.Primary,
        wildcard: false,
        zone: 'zone2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        domain: 'domain6',
        minimumTlsVersion: MinimumTlsVersion.Enum12,
        type: Type1.Primary,
        wildcard: false,
        zone: 'zone2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    functions: [
      {
        name: 'name4',
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
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    jobs: [
      {
        name: 'name4',
        buildCommand: 'build_command8',
        dockerfilePath: 'dockerfile_path6',
        environmentSlug: 'environment_slug2',
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
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    region: Region1.Nyc,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  appId: 'b6bdf840-2854-4f87-a36c-5f231c617c84',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



