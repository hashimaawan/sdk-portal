# V2 Kubernetes Clusters Upgrades Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersUpgradesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available_upgrade_versions` | [`Array[AvailableUpgradeVersion]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/available-upgrade-version.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_upgrades_response = V2KubernetesClustersUpgradesResponse.new(
  available_upgrade_versions: [
    AvailableUpgradeVersion.new(
      kubernetes_version: 'kubernetes_version0',
      slug: 'slug2',
      supported_features: [
        'supported_features3'
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AvailableUpgradeVersion.new(
      kubernetes_version: 'kubernetes_version0',
      slug: 'slug2',
      supported_features: [
        'supported_features3'
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



