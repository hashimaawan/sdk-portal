# Git

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkdpdA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Git`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `String` | Optional | The name of the branch to use |
| `repo_clone_url` | `String` | Optional | The clone URL of the repo. Example: `https://github.com/digitalocean/sample-golang.git` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
git = Git.new(
  branch: 'main',
  repo_clone_url: 'https://github.com/digitalocean/sample-golang.git',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



