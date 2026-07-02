# V2 Kubernetes Clusters Clusterlint Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completed_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was completed. |
| `diagnostics` | [`Array[Diagnostic]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/diagnostic.md) | Optional | An array of diagnostics reporting potential problems for the given cluster. |
| `requested_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was made. |
| `run_id` | `String` | Optional | Id of the clusterlint run that can be used later to fetch the diagnostics. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_clusterlint_response = V2KubernetesClustersClusterlintResponse.new(
  completed_at: DateTimeHelper.from_rfc3339('2019-10-30T05:34:11Z'),
  diagnostics: [
    Diagnostic.new(
      check_name: 'check_name8',
      message: 'message2',
      object: Object.new(
        kind: 'kind0',
        name: 'name2',
        namespace: 'namespace0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      severity: 'severity2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  requested_at: DateTimeHelper.from_rfc3339('2019-10-30T05:34:07Z'),
  run_id: '50c2f44c-011d-493e-aee5-361a4a0d1844',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



