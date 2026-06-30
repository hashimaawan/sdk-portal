# Get Server Health

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldFNlcnZlckhlYWx0aA

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetServerHealthAsync()
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.HealthResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/health-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<HealthResponse> result = await healthApi.GetServerHealthAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Example Response *(as JSON)*

```json
{
  "dependencies": [
    {
      "service": "sync",
      "status": "TOKEN_NEEDED"
    },
    {
      "message": "Connected to./1password.sqlite",
      "service": "sqlite",
      "status": "ACTIVE"
    }
  ],
  "name": "1Password Connect API",
  "version": "1.2.1"
}
```



