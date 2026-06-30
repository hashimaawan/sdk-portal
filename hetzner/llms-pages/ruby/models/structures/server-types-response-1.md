# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server_type` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-type.md) | Required | - |


# Example

```ruby
server_types_response1 = ServerTypesResponse1.new(
  ServerType.new(
    1,
    CpuTypeEnum::SHARED,
    false,
    'CX11',
    24,
    1,
    1,
    'cx11',
    [
      Price9.new(
        'fsn1',
        PriceHourly8.new(
          '1.1900000000000000',
          '1.0000000000'
        ),
        PriceMonthly10.new(
          '1.1900000000000000',
          '1.0000000000'
        )
      )
    ],
    StorageTypeEnum::LOCAL
  )
)
```



