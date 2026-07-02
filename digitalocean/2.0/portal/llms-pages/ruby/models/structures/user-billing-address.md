# User Billing Address

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlVzZXJCaWxsaW5nQWRkcmVzcw

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`UserBillingAddress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address_line_1` | `String` | Optional | Street address line 1 |
| `address_line_2` | `String` | Optional | Street address line 2 |
| `city` | `String` | Optional | City |
| `country_iso_2_code` | `String` | Optional | Country (ISO2) code |
| `created_at` | `String` | Optional | Timestamp billing address was created |
| `postal_code` | `String` | Optional | Postal code |
| `region` | `String` | Optional | Region |
| `updated_at` | `String` | Optional | Timestamp billing address was updated |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
user_billing_address = UserBillingAddress.new(
  address_line1: '101 Shark Row',
  address_line2: 'address_line26',
  city: 'Atlantis',
  country_iso2_code: 'US',
  created_at: '2019-09-03T16:34:46.000+00:00',
  postal_code: '12345',
  region: 'OC',
  updated_at: '2019-09-03T16:34:46.000+00:00',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



