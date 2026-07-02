# Load Balancers Add Droplets

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRmxvYWRCYWxhbmNlcnNfYWRkX2Ryb3BsZXRz

To assign a Droplet to a load balancer instance, send a POST request to
`/v2/load_balancers/$LOAD_BALANCER_ID/droplets`. In the body of the request,
there should be a `droplet_ids` attribute containing a list of Droplet IDs.
Individual Droplets can not be added to a load balancer configured with a
Droplet tag. Attempting to do so will result in a "422 Unprocessable Entity"
response from the API.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.

```csharp
LoadBalancersAddDropletsAsync(
    string lbId,
    Models.V2LoadBalancersDropletsRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lbId` | `string` | Template, Required | A unique identifier for a load balancer. |
| `body` | [`V2LoadBalancersDropletsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-load-balancers-droplets-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`Task`


# Example Usage

```csharp
string lbId = "4de7ac8b-495b-4884-9a69-1050c6793cd6";
V2LoadBalancersDropletsRequest body = new V2LoadBalancersDropletsRequest
{
    DropletIds = new List<int>
    {
        3164444,
        3164445,
    },
};

try
{
    await loadBalancersApi.LoadBalancersAddDropletsAsync(
        lbId,
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



