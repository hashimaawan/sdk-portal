# V2 Databases Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9wdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `options` | [`Options`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/options.md) | Optional | - |
| `version_availability` | [`VersionAvailability`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/version-availability.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_options_response = V2DatabasesOptionsResponse.new(
  options: Options.new(
    mongodb: Mongodb.new(
      regions: [
        'regions3',
        'regions4'
      ],
      versions: [
        'versions3',
        'versions4'
      ],
      layouts: [
        Layout.new(
          num_nodes: 190,
          sizes: [
            'sizes2',
            'sizes3'
          ],
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Layout.new(
          num_nodes: 190,
          sizes: [
            'sizes2',
            'sizes3'
          ],
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    mysql: Mysql.new(
      regions: [
        'regions9',
        'regions0',
        'regions1'
      ],
      versions: [
        'versions9',
        'versions0',
        'versions1'
      ],
      layouts: [
        Layout.new(
          num_nodes: 190,
          sizes: [
            'sizes2',
            'sizes3'
          ],
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Layout.new(
          num_nodes: 190,
          sizes: [
            'sizes2',
            'sizes3'
          ],
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Layout.new(
          num_nodes: 190,
          sizes: [
            'sizes2',
            'sizes3'
          ],
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    pg: Pg.new(
      regions: [
        'regions3'
      ],
      versions: [
        'versions3'
      ],
      layouts: [
        Layout.new(
          num_nodes: 190,
          sizes: [
            'sizes2',
            'sizes3'
          ],
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    redis: Redis.new(
      regions: [
        'regions7'
      ],
      versions: [
        'versions7'
      ],
      layouts: [
        Layout.new(
          num_nodes: 190,
          sizes: [
            'sizes2',
            'sizes3'
          ],
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
  ),
  version_availability: VersionAvailability.new(
    mongodb: [
      Mongodb1.new(
        end_of_availability: 'end_of_availability4',
        end_of_life: 'end_of_life4',
        version: 'version4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Mongodb1.new(
        end_of_availability: 'end_of_availability4',
        end_of_life: 'end_of_life4',
        version: 'version4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    mysql: [
      Mongodb1.new(
        end_of_availability: 'end_of_availability0',
        end_of_life: 'end_of_life0',
        version: 'version0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Mongodb1.new(
        end_of_availability: 'end_of_availability0',
        end_of_life: 'end_of_life0',
        version: 'version0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    pg: [
      Mongodb1.new(
        end_of_availability: 'end_of_availability4',
        end_of_life: 'end_of_life4',
        version: 'version4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    redis: [
      Mongodb1.new(
        end_of_availability: 'end_of_availability8',
        end_of_life: 'end_of_life8',
        version: 'version8',
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



