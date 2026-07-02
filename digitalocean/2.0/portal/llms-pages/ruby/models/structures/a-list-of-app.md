# A List of App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkElMjUyMGxpc3QlMjUyMG9mJTI1MjBhcHA

An application's configuration and status.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`AListOfApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active_deployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/an-app-deployment.md) | Optional | - |
| `created_at` | `DateTime` | Optional, Read-only | - |
| `default_ingress` | `String` | Optional, Read-only | - |
| `domains` | [`Array[ContainsAllDomainsForTheApp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/contains-all-domains-for-the-app.md) | Optional, Read-only | - |
| `id` | `String` | Optional, Read-only | - |
| `in_progress_deployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/an-app-deployment.md) | Optional | - |
| `last_deployment_created_at` | `DateTime` | Optional, Read-only | - |
| `live_domain` | `String` | Optional, Read-only | - |
| `live_url` | `String` | Optional, Read-only | - |
| `live_url_base` | `String` | Optional, Read-only | - |
| `owner_uuid` | `String` | Optional, Read-only | - |
| `pending_deployment` | [`PendingDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/pending-deployment.md) | Optional | - |
| `pinned_deployment` | [`PinnedDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/pinned-deployment.md) | Optional | - |
| `project_id` | `String` | Optional, Read-only | - |
| `region` | [`GeographicalInformationAboutAnAppOrigin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/geographical-information-about-an-app-origin.md) | Optional | - |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `tier_slug` | `String` | Optional, Read-only | - |
| `updated_at` | `DateTime` | Optional, Read-only | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
a_list_of_app = AListOfApp.new(
  spec: AppSpec.new(
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
      ),
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
      )
    ],
    region: Region1::NYC,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  active_deployment: AnAppDeployment.new(
    cause: 'cause6',
    cloned_from: 'cloned_from2',
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    functions: [
      FunctionsComponentsThatArePartOfThisDeployment.new(
        name: 'name4',
        namespace: 'namespace8',
        source_commit_hash: 'source_commit_hash4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      FunctionsComponentsThatArePartOfThisDeployment.new(
        name: 'name4',
        namespace: 'namespace8',
        source_commit_hash: 'source_commit_hash4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      FunctionsComponentsThatArePartOfThisDeployment.new(
        name: 'name4',
        namespace: 'namespace8',
        source_commit_hash: 'source_commit_hash4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    id: 'id0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  created_at: DateTimeHelper.from_rfc3339('2020-11-19T20:27:18Z'),
  default_ingress: 'digitalocean.com',
  domains: [
    ContainsAllDomainsForTheApp.new(
      certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      id: 'id0',
      phase: Phase1::CONFIGURING,
      progress: Progress1.new(
        steps: [
          { 'key1' => 'val1', 'key2' => 'val2' },
          { 'key1' => 'val1', 'key2' => 'val2' },
          { 'key1' => 'val1', 'key2' => 'val2' }
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      rotate_validation_records: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    ContainsAllDomainsForTheApp.new(
      certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      id: 'id0',
      phase: Phase1::CONFIGURING,
      progress: Progress1.new(
        steps: [
          { 'key1' => 'val1', 'key2' => 'val2' },
          { 'key1' => 'val1', 'key2' => 'val2' },
          { 'key1' => 'val1', 'key2' => 'val2' }
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      rotate_validation_records: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  id: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  last_deployment_created_at: DateTimeHelper.from_rfc3339('2020-11-19T20:27:18Z'),
  live_domain: 'live_domain',
  live_url: 'google.com',
  live_url_base: 'digitalocean.com',
  owner_uuid: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  project_id: '88b72d1a-b78a-4d9f-9090-b53c4399073f',
  tier_slug: 'basic',
  updated_at: DateTimeHelper.from_rfc3339('2020-12-01T00:42:16Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



