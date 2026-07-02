# App Spec

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcFNwZWM

The desired configuration of an application.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`AppSpec`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databases` | [`Array[Database]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/database.md) | Optional | Database instances which can provide persistence to workloads within the<br>application. |
| `domains` | [`Array[Domain]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/domain.md) | Optional | A set of hostnames where the application will be available. |
| `functions` | [`Array[Function]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/function.md) | Optional | Workloads which expose publicly-accessible HTTP services via Functions Components. |
| `jobs` | [`Array[Job]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/job.md) | Optional | Pre and post deployment workloads which do not expose publicly-accessible HTTP routes. |
| `name` | `String` | Required | The name of the app. Must be unique across all apps in the same account.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `region` | [`Region1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/region-1.md) | Optional | The slug form of the geographical origin of the app. Default: `nearest available` |
| `services` | [`Array[Service]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/service.md) | Optional | Workloads which expose publicly-accessible HTTP services. |
| `static_sites` | [`Array[StaticSite]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/static-site.md) | Optional | Content which can be rendered to static web assets. |
| `workers` | [`Array[Worker]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/worker.md) | Optional | Workloads which do not expose publicly-accessible HTTP services. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
app_spec = AppSpec.new(
  name: 'web-app-01',
  databases: [
    Database.new(
      name: 'name6',
      cluster_name: 'cluster_name8',
      db_name: 'db_name0',
      db_user: 'db_user8',
      engine: Engine::PG,
      production: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Database.new(
      name: 'name6',
      cluster_name: 'cluster_name8',
      db_name: 'db_name0',
      db_user: 'db_user8',
      engine: Engine::PG,
      production: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Database.new(
      name: 'name6',
      cluster_name: 'cluster_name8',
      db_name: 'db_name0',
      db_user: 'db_user8',
      engine: Engine::PG,
      production: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  domains: [
    Domain.new(
      domain: 'domain6',
      minimum_tls_version: MinimumTlsVersion::ENUM_12,
      type: Type1::PRIMARY,
      wildcard: false,
      zone: 'zone2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  functions: [
    Function.new(
      name: 'name4',
      alerts: [
        Alert.new(
          disabled: false,
          operator: Operator::LESS_THAN,
          rule: Rule::MEM_UTILIZATION,
          value: 12.58,
          window: Window::THIRTY_MINUTES,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      cors: Cors.new(
        allow_credentials: false,
        allow_headers: [
          'allow_headers9',
          'allow_headers0'
        ],
        allow_methods: [
          'allow_methods8',
          'allow_methods9',
          'allow_methods0'
        ],
        allow_origins: [
          nil
        ],
        expose_headers: [
          'expose_headers2'
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      envs: [
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      git: Git.new(
        branch: 'branch8',
        repo_clone_url: 'repo_clone_url8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      github: Github.new(
        branch: 'branch4',
        deploy_on_push: false,
        repo: 'repo6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Function.new(
      name: 'name4',
      alerts: [
        Alert.new(
          disabled: false,
          operator: Operator::LESS_THAN,
          rule: Rule::MEM_UTILIZATION,
          value: 12.58,
          window: Window::THIRTY_MINUTES,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      cors: Cors.new(
        allow_credentials: false,
        allow_headers: [
          'allow_headers9',
          'allow_headers0'
        ],
        allow_methods: [
          'allow_methods8',
          'allow_methods9',
          'allow_methods0'
        ],
        allow_origins: [
          nil
        ],
        expose_headers: [
          'expose_headers2'
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      envs: [
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      git: Git.new(
        branch: 'branch8',
        repo_clone_url: 'repo_clone_url8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      github: Github.new(
        branch: 'branch4',
        deploy_on_push: false,
        repo: 'repo6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Function.new(
      name: 'name4',
      alerts: [
        Alert.new(
          disabled: false,
          operator: Operator::LESS_THAN,
          rule: Rule::MEM_UTILIZATION,
          value: 12.58,
          window: Window::THIRTY_MINUTES,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      cors: Cors.new(
        allow_credentials: false,
        allow_headers: [
          'allow_headers9',
          'allow_headers0'
        ],
        allow_methods: [
          'allow_methods8',
          'allow_methods9',
          'allow_methods0'
        ],
        allow_origins: [
          nil
        ],
        expose_headers: [
          'expose_headers2'
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      envs: [
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      git: Git.new(
        branch: 'branch8',
        repo_clone_url: 'repo_clone_url8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      github: Github.new(
        branch: 'branch4',
        deploy_on_push: false,
        repo: 'repo6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  jobs: [
    Job.new(
      name: 'name4',
      build_command: 'build_command8',
      dockerfile_path: 'dockerfile_path6',
      environment_slug: 'environment_slug2',
      envs: [
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      git: Git.new(
        branch: 'branch8',
        repo_clone_url: 'repo_clone_url8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Job.new(
      name: 'name4',
      build_command: 'build_command8',
      dockerfile_path: 'dockerfile_path6',
      environment_slug: 'environment_slug2',
      envs: [
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      git: Git.new(
        branch: 'branch8',
        repo_clone_url: 'repo_clone_url8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Job.new(
      name: 'name4',
      build_command: 'build_command8',
      dockerfile_path: 'dockerfile_path6',
      environment_slug: 'environment_slug2',
      envs: [
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Env.new(
          key: 'key2',
          scope: Scope::UNSET,
          type: Type2::GENERAL,
          value: 'value4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      git: Git.new(
        branch: 'branch8',
        repo_clone_url: 'repo_clone_url8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  region: Region1::NYC,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



