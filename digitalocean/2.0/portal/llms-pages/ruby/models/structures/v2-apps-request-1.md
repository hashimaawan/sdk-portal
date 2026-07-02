# V2 Apps Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_request1 = V2AppsRequest1.new(
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
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



