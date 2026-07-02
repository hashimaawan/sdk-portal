# V2 Apps Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app` | [`AListOfApp \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/a-list-of-app.md) | Optional | An application's configuration and status. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Engine,
  MinimumTlsVersion,
  Operator,
  Phase1,
  Region1,
  Rule,
  Scope,
  Type1,
  Type2,
  V2AppsResponse1,
  Window,
} from 'digitalocean-apilib';

const v2AppsResponse1: V2AppsResponse1 = {
  app: {
    spec: {
      name: 'name2',
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
      region: Region1.Blr,
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
    createdAt: '2016-03-13T12:52:32.123Z',
    defaultIngress: 'default_ingress8',
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
    id: 'id2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



