# Trip GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlRyaXBfR0VU

list user's trips

```csharp
TripGetAsync()
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Requires scope

## furkot_auth_access_code

`read:trips`

## furkot_auth_implicit

`read:trips`


# Response Type

**200**: Successful response

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [List<Models.Trip>](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/models/structures/trip.md).


# Example Usage

```csharp
try
{
    ApiResponse<List<Trip>> result = await api.TripGetAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



