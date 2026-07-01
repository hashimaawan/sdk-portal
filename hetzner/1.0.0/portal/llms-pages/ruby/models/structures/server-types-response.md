# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server_types` | [`Array[ServerTypes7]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-types-7.md) | Required | - |


# Example

```ruby
server_types_response = ServerTypesResponse.new(
  [
    ServerTypes7.new(
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
  ]
)
```



