# Delete a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGRGVsZXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Deletes a PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```csharp
DeleteAPlacementGroupAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: PlacementGroup deleted

`Task`


# Example Usage

```csharp
int id = 112;
try
{
    await placementGroupsApi.DeleteAPlacementGroupAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



