# Function

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkZ1bmN0aW9u

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Function`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alerts` | [`Array[Alert]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/alert.md) | Optional | - |
| `cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/cors.md) | Optional | - |
| `envs` | [`Array[Env]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `git` | [`Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/git.md) | Optional | - |
| `github` | [`Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/github.md) | Optional | - |
| `gitlab` | [`Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/gitlab.md) | Optional | - |
| `log_destinations` | [`ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/configurations-for-external-logging.md) | Optional | - |
| `name` | `String` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `routes` | [`Array[ACriterionForRoutingHttpTrafficToAComponent]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `source_dir` | `String` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
function = Function.new(
  name: 'api',
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
    ),
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
  source_dir: 'path/to/dir',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



