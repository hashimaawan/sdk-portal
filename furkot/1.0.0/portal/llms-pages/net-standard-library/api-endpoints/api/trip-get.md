# Trip GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlRyaXBfR0VU

list user's trips

```csharp
TripGETAsync()
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/authorization.md)


# Requires scope

## furkot_auth_access_code

`read:trips`

## furkot_auth_implicit

`read:trips`


# Response Type

**200**: Successful response

[`Task<List<Models.Trip>>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/models/structures/trip.md)


# Example Usage

```csharp
try
{
    List<Trip> result = await aPIController.TripGETAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



