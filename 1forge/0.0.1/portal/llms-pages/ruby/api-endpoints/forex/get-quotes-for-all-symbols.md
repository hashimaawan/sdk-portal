# Get Quotes for All Symbols

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/ruby/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBxdW90ZXMlMjUyMGZvciUyNTIwYWxsJTI1MjBzeW1ib2xz

Get quotes

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_quotes_for_all_symbols
```


# Response Type

**200**: A list of quotes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
result = forex_api.get_quotes_for_all_symbols

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



