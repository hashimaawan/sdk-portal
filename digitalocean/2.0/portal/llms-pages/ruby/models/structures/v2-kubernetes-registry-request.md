# V2 Kubernetes Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesRegistryRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cluster_uuids` | `Array[String]` | Optional | An array containing the UUIDs of Kubernetes clusters. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_registry_request = V2KubernetesRegistryRequest.new(
  cluster_uuids: [
    'bd5f5959-5e1e-4205-a714-a914373942af',
    '50c2f44c-011d-493e-aee5-361a4a0d1844'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



