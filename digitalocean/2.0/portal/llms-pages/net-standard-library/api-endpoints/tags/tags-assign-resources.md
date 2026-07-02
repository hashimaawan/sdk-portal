# Tags Assign Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlRhZ3MlMkZ0YWdzX2Fzc2lnbl9yZXNvdXJjZXM

Resources can be tagged by sending a POST request to `/v2/tags/$TAG_NAME/resources` with an array of json objects containing `resource_id` and `resource_type` attributes.
Currently only tagging of Droplets, Databases, Images, Volumes, and Volume Snapshots is supported. `resource_type` is expected to be the string `droplet`, `database`, `image`, `volume` or `volume_snapshot`. `resource_id` is expected to be the ID of the resource as a string.

```csharp
TagsAssignResourcesAsync(
    string tagId,
    Models.V2TagsResourcesRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tagId` | `string` | Template, Required | The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores. There is a limit of 255 characters per tag.<br><br>**Constraints**: *Maximum Length*: `255`, *Pattern*: `^[a-zA-Z0-9_\-\:]+$` |
| `body` | [`V2TagsResourcesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-tags-resources-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`Task`


# Example Usage

```csharp
string tagId = "awesome";
V2TagsResourcesRequest body = new V2TagsResourcesRequest
{
    Resources = new List<Resources3>
    {
        new Resources3
        {
            ResourceId = "9569411",
            ResourceType = ResourceType2.Droplet,
        },
        new Resources3
        {
            ResourceId = "7555620",
            ResourceType = ResourceType2.Image,
        },
        new Resources3
        {
            ResourceId = "3d80cb72-342b-4aaa-b92e-4e4abb24a933",
            ResourceType = ResourceType2.Volume,
        },
    },
};

try
{
    await tagsApi.TagsAssignResourcesAsync(
        tagId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V21Clicks401ErrorException)
    {
       // TODO: Handle V21Clicks401ErrorException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



