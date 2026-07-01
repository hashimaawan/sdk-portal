# Get Quotes for All Symbols

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/net-standard-library/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBxdW90ZXMlMjUyMGZvciUyNTIwYWxsJTI1MjBzeW1ib2xz

Get quotes

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetQuotesForAllSymbolsAsync()
```


# Response Type

**200**: A list of quotes

`Task`


# Example Usage

```csharp
try
{
    await forexController.GetQuotesForAllSymbolsAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



