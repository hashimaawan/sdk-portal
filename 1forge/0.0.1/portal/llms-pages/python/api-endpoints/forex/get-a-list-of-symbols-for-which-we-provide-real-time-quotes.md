# Get a List of Symbols for Which We Provide Real-Time Quotes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/python/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBhJTI1MjBsaXN0JTI1MjBvZiUyNTIwc3ltYm9scyUyNTIwZm9yJTI1MjB3aGljaCUyNTIwd2UlMjUyMHByb3ZpZGUlMjUyMHJlYWwtdGltZSUyNTIwcXVvdGVz

Symbol List

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_list_of_symbols_for_which_we_provide_real_time_quotes(self)
```


# Response Type

**200**: A list of symbols

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type `List[str]`.


# Example Usage

```python
result = forex_api.get_a_list_of_symbols_for_which_we_provide_real_time_quotes()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



