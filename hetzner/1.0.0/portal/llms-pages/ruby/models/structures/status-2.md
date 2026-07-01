# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened |
| `issuance` | [`IssuanceEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate |
| `renewal` | [`RenewalEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. |


# Example

```ruby
status2 = Status2.new(
  nil,
  IssuanceEnum::COMPLETED,
  RenewalEnum::SCHEDULED
)
```



