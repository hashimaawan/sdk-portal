# Available Upgrade Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkF2YWlsYWJsZVVwZ3JhZGVWZXJzaW9u

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`AvailableUpgradeVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetes_version` | `String` | Optional | The upstream version string for the version of Kubernetes provided by a given slug. |
| `slug` | `String` | Optional | The slug identifier for an available version of Kubernetes for use when creating or updating a cluster. The string contains both the upstream version of Kubernetes as well as the DigitalOcean revision. |
| `supported_features` | `Array[String]` | Optional | The features available with the version of Kubernetes provided by a given slug. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
available_upgrade_version = AvailableUpgradeVersion.new(
  kubernetes_version: '1.16.13',
  slug: '1.16.13-do.0',
  supported_features: [
    'cluster-autoscaler',
    'docr-integration',
    'token-authentication'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



