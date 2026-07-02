# Action 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFjdGlvbjE

The linked actions can be used to check the status of a Droplet's create event.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Action1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Optional | A URL that can be used to access the action. |
| `id` | `Integer` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `rel` | `String` | Optional | A string specifying the type of the related action. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
action1 = Action1.new(
  href: 'https://api.digitalocean.com/v2/actions/7515',
  id: 7515,
  rel: 'create',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



