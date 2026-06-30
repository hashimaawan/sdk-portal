# Trip Stop by Trip Id GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlRyaXBTdG9wQnlUcmlwSWRfR0VU

list stops for a trip identified by {trip_id}

```csharp
TripStopByTripIdGETAsync(
    string tripId)
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/net-standard-library/getting-started/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/net-standard-library/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tripId` | `string` | Template, Required | id of the trip |


# Requires scope

## furkot_auth_access_code

`read:trips`

## furkot_auth_implicit

`read:trips`


# Response Type

**200**: Successful response

[`Task<List<Models.Step>>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/net-standard-library/models/structures/step.md)


# Example Usage

```csharp
string tripId = "trip_id2";
try
{
    List<Step> result = await aPIController.TripStopByTripIdGETAsync(tripId);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



