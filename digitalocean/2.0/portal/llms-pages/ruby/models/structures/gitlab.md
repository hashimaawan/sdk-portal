# Gitlab

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkdpdGxhYg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Gitlab`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `String` | Optional | The name of the branch to use |
| `deploy_on_push` | `TrueClass \| FalseClass` | Optional | Whether to automatically deploy new commits made to the repo |
| `repo` | `String` | Optional | The name of the repo in the format owner/repo. Example: `digitalocean/sample-golang` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
gitlab = Gitlab.new(
  branch: 'main',
  deploy_on_push: true,
  repo: 'digitalocean/sample-golang',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



