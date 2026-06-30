# Get Heartbeat

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldEhlYXJ0YmVhdA

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetHeartbeatAsync()
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type string.


# Example Usage

```csharp
try
{
    ApiResponse<string> result = await healthApi.GetHeartbeatAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



