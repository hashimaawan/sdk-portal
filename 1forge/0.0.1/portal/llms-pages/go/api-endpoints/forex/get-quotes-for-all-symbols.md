# Get Quotes for All Symbols

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/go/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBxdW90ZXMlMjUyMGZvciUyNTIwYWxsJTI1MjBzeW1ib2xz

Get quotes

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```go
GetQuotesForAllSymbols(
    ctx context.Context) (
    http.Response,
    error)
```


# Response Type

**200**: A list of quotes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

resp, err := forexApi.GetQuotesForAllSymbols(ctx)
if err != nil {
    log.Fatalln(err)
} else {
    fmt.Println(resp.StatusCode)
}
```



