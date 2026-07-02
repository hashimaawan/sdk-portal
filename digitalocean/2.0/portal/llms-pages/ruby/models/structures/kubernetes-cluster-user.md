# Kubernetes Cluster User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVyVXNlcg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`KubernetesClusterUser`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `groups` | `Array[String]` | Optional | A list of in-cluster groups that the user belongs to. |
| `username` | `String` | Optional | The username for the cluster admin user. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
kubernetes_cluster_user = KubernetesClusterUser.new(
  groups: [
    'k8saas:authenticated'
  ],
  username: 'sammy@digitalocean.com',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



