# App Spec

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcFNwZWM

The desired configuration of an application.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`AppSpec`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databases` | [`Database[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/database.md) | Optional | Database instances which can provide persistence to workloads within the<br>application. |
| `domains` | [`Domain[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/domain.md) | Optional | A set of hostnames where the application will be available. |
| `functions` | [`Function[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/function.md) | Optional | Workloads which expose publicly-accessible HTTP services via Functions Components. |
| `jobs` | [`Job[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/job.md) | Optional | Pre and post deployment workloads which do not expose publicly-accessible HTTP routes. |
| `name` | `string` | Required | The name of the app. Must be unique across all apps in the same account.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `region` | [`Region1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/region-1.md) | Optional | The slug form of the geographical origin of the app. Default: `nearest available` |
| `services` | [`Service[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/service.md) | Optional | Workloads which expose publicly-accessible HTTP services. |
| `staticSites` | [`StaticSite[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/static-site.md) | Optional | Content which can be rendered to static web assets. |
| `workers` | [`Worker[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/worker.md) | Optional | Workloads which do not expose publicly-accessible HTTP services. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  AppSpec,
  Engine,
  MinimumTlsVersion,
  Operator,
  Region1,
  Rule,
  Scope,
  Type1,
  Type2,
  Window,
} from 'digitalocean-apilib';

const appSpec: AppSpec = {
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
    },
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
    },
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
    },
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
};
```



