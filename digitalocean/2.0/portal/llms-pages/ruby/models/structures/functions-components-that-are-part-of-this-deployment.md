# Functions Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkZ1bmN0aW9ucyUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`FunctionsComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | - |
| `namespace` | `String` | Optional | The namespace where the functions are deployed. |
| `source_commit_hash` | `String` | Optional | The commit hash of the repository that was used to build this functions component. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
functions_components_that_are_part_of_this_deployment = FunctionsComponentsThatArePartOfThisDeployment.new(
  name: 'my-functions-component',
  namespace: 'ap-b2a93513-8d9b-4223-9d61-5e7272c81c32',
  source_commit_hash: '54d4a727f457231062439895000d45437c7bb405',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



