# V2 Droplets Destroy with Associated Resources Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTdGF0dXMlMjUyMFJlc3BvbnNl

An objects containing information about a resources scheduled for deletion.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completed_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format indicating when the requested action was completed. |
| `droplet` | [`Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet-1.md) | Optional | An object containing information about a resource scheduled for deletion. |
| `failures` | `Integer` | Optional | A count of the associated resources that failed to be destroyed, if any. |
| `resources` | [`Resources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/resources.md) | Optional | An object containing additional information about resource related to a Droplet requested to be destroyed. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_droplets_destroy_with_associated_resources_status_response = V2DropletsDestroyWithAssociatedResourcesStatusResponse.new(
  completed_at: DateTimeHelper.from_rfc3339('2020-04-01T18:11:49Z'),
  droplet: Droplet1.new(
    destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    error_message: 'error_message2',
    id: 'id0',
    name: 'name0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  failures: 0,
  resources: Resources.new(
    floating_ips: [
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message4',
        id: 'id2',
        name: 'name2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message4',
        id: 'id2',
        name: 'name2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message4',
        id: 'id2',
        name: 'name2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    reserved_ips: [
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message2',
        id: 'id0',
        name: 'name0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message2',
        id: 'id0',
        name: 'name0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    snapshots: [
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message4',
        id: 'id2',
        name: 'name2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message4',
        id: 'id2',
        name: 'name2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message4',
        id: 'id2',
        name: 'name2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    volume_snapshots: [
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message0',
        id: 'id8',
        name: 'name8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message0',
        id: 'id8',
        name: 'name8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    volumes: [
      Droplet1.new(
        destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        error_message: 'error_message8',
        id: 'id6',
        name: 'name6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



