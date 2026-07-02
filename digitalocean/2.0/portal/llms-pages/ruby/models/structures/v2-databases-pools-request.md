# V2 Databases Pools Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesPoolsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `db` | `String` | Required | The database for use with the connection pool. |
| `mode` | `String` | Required | The PGBouncer transaction mode for the connection pool. The allowed values are session, transaction, and statement. |
| `size` | `Integer` | Required | The desired size of the PGBouncer connection pool. The maximum allowed size is determined by the size of the cluster's primary node. 25 backend server connections are allowed for every 1GB of RAM. Three are reserved for maintenance. For example, a primary node with 1 GB of RAM allows for a maximum of 22 backend server connections while one with 4 GB would allow for 97. Note that these are shared across all connection pools in a cluster. |
| `user` | `String` | Optional | The name of the user for use with the connection pool. When excluded, all sessions connect to the database as the inbound user. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_pools_request = V2DatabasesPoolsRequest.new(
  db: 'defaultdb',
  mode: 'transaction',
  size: 10,
  user: 'doadmin',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



