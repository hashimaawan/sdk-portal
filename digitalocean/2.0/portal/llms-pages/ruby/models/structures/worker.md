# Worker

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRldvcmtlcg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Worker`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `build_command` | `String` | Optional | An optional build command to run while building this component from source. |
| `dockerfile_path` | `String` | Optional | The path to the Dockerfile relative to the root of the repo. If set, it will be used to build this component. Otherwise, App Platform will attempt to build it using buildpacks. |
| `environment_slug` | `String` | Optional | An environment slug describing the type of this app. For a full list, please refer to [the product documentation](https://www.digitalocean.com/docs/app-platform/). |
| `envs` | [`Array[Env]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `git` | [`Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/git.md) | Optional | - |
| `github` | [`Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/github.md) | Optional | - |
| `gitlab` | [`Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/gitlab.md) | Optional | - |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `log_destinations` | [`ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/configurations-for-external-logging.md) | Optional | - |
| `name` | `String` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `run_command` | `String` | Optional | An optional run command to override the component's default. |
| `source_dir` | `String` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `instance_count` | `Integer` | Optional | The amount of instances that this component should be scaled to. Default: 1<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `instance_size_slug` | [`InstanceSizeSlug`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/instance-size-slug.md) | Optional | The instance size to use for this component. Default: `basic-xxs`<br><br>**Default**: `InstanceSizeSlug::BASICXXS` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
worker = Worker.new(
  name: 'api',
  build_command: 'npm run build',
  dockerfile_path: 'path/to/Dockerfile',
  environment_slug: 'node-js',
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
  run_command: 'bin/api',
  source_dir: 'path/to/dir',
  instance_count: 2,
  instance_size_slug: InstanceSizeSlug::BASICXXS,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



