# Get a Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvY2F0aW9ucyUyRkdldCUyNTIwYSUyNTIwTG9jYXRpb24

Returns a specific Location object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetALocationAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Location |


# Response Type

**200**: The `location` key in the reply contains a Location object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.LocationsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/locations-response-1.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<LocationsResponse1> result = await locationsApi.GetALocationAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



