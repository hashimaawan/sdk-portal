# A List of App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkElMjUyMGxpc3QlMjUyMG9mJTI1MjBhcHA

An application's configuration and status.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`AListOfApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `activeDeployment` | [`AnAppDeployment \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/an-app-deployment.md) | Optional | - |
| `createdAt` | `string \| undefined` | Optional, Read-only | - |
| `defaultIngress` | `string \| undefined` | Optional, Read-only | - |
| `domains` | [`ContainsAllDomainsForTheApp[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/contains-all-domains-for-the-app.md) | Optional, Read-only | - |
| `id` | `string \| undefined` | Optional, Read-only | - |
| `inProgressDeployment` | [`AnAppDeployment \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/an-app-deployment.md) | Optional | - |
| `lastDeploymentCreatedAt` | `string \| undefined` | Optional, Read-only | - |
| `liveDomain` | `string \| undefined` | Optional, Read-only | - |
| `liveUrl` | `string \| undefined` | Optional, Read-only | - |
| `liveUrlBase` | `string \| undefined` | Optional, Read-only | - |
| `ownerUuid` | `string \| undefined` | Optional, Read-only | - |
| `pendingDeployment` | [`PendingDeployment \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/pending-deployment.md) | Optional | - |
| `pinnedDeployment` | [`PinnedDeployment \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/pinned-deployment.md) | Optional | - |
| `projectId` | `string \| undefined` | Optional, Read-only | - |
| `region` | [`GeographicalInformationAboutAnAppOrigin \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/geographical-information-about-an-app-origin.md) | Optional | - |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `tierSlug` | `string \| undefined` | Optional, Read-only | - |
| `updatedAt` | `string \| undefined` | Optional, Read-only | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  AListOfApp,
  Engine,
  MinimumTlsVersion,
  Operator,
  Phase1,
  Region1,
  Rule,
  Scope,
  Type1,
  Type2,
  Window,
} from 'digitalocean-apilib';

const aListOfApp: AListOfApp = {
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
  activeDeployment: {
    cause: 'cause6',
    clonedFrom: 'cloned_from2',
    createdAt: '2016-03-13T12:52:32.123Z',
    functions: [
      {
        name: 'name4',
        namespace: 'namespace8',
        sourceCommitHash: 'source_commit_hash4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        name: 'name4',
        namespace: 'namespace8',
        sourceCommitHash: 'source_commit_hash4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        name: 'name4',
        namespace: 'namespace8',
        sourceCommitHash: 'source_commit_hash4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    id: 'id0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  createdAt: '2020-11-19T20:27:18Z',
  defaultIngress: 'digitalocean.com',
  domains: [
    {
      certificateExpiresAt: '2016-03-13T12:52:32.123Z',
      id: 'id0',
      phase: Phase1.Configuring,
      progress: {
        steps: [
          { 'key1': 'val1', 'key2': 'val2' },
          { 'key1': 'val1', 'key2': 'val2' },
          { 'key1': 'val1', 'key2': 'val2' }
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      rotateValidationRecords: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  id: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  lastDeploymentCreatedAt: '2020-11-19T20:27:18Z',
  liveDomain: 'live_domain',
  liveUrl: 'google.com',
  liveUrlBase: 'digitalocean.com',
  ownerUuid: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  projectId: '88b72d1a-b78a-4d9f-9090-b53c4399073f',
  tierSlug: 'basic',
  updatedAt: '2020-12-01T00:42:16Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



