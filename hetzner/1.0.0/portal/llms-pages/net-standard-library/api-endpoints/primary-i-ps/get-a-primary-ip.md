# Get a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Returns a specific Primary IP object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAPrimaryIPAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `primary_ip` key contains a Primary IP object

[`Task<Models.PrimaryIPResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/primary-ip-response.md)


# Example Usage

```csharp
int id = 112;
try
{
    PrimaryIPResponse result = await primaryIPsController.GetAPrimaryIPAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



