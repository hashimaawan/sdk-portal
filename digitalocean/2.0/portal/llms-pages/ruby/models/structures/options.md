# Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk9wdGlvbnM

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Options`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mongodb` | [`Mongodb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/mongodb.md) | Optional | - |
| `mysql` | [`Mysql`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/mysql.md) | Optional | - |
| `pg` | [`Pg`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/pg.md) | Optional | - |
| `redis` | [`Redis`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/redis.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
options = Options.new(
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
)
```



