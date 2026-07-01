# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `Array[Float]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `available_for_migration` | `Array[Float]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `supported` | `Array[Float]` | Required | IDs of Server types that are supported in the Datacenter |


# Example

```ruby
server_types = ServerTypes.new(
  [
    1,
    2,
    3
  ],
  [
    1,
    2,
    3
  ],
  [
    1,
    2,
    3
  ]
)
```



