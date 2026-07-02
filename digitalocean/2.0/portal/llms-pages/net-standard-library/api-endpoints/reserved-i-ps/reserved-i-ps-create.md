# Reserved I Ps Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlJlc2VydmVkJTI1MjBJUHMlMkZyZXNlcnZlZElQc19jcmVhdGU

On creation, a reserved IP must be either assigned to a Droplet or reserved to a region.

* To create a new reserved IP assigned to a Droplet, send a POST
  request to `/v2/reserved_ips` with the `droplet_id` attribute.

* To create a new reserved IP reserved to a region, send a POST request to
  `/v2/reserved_ips` with the `region` attribute.

**Note**:  In addition to the standard rate limiting, only 12 reserved IPs may be created per 60 seconds.

```csharp
ReservedIPsCreateAsync(
    ReservedIPsCreateBody body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`ReservedIPsCreateBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/reserved-i-ps-create-body.md) | Body, Required | This is a container for one-of cases. |


# Response Type

**202**: The response will be a JSON object with a key called `reserved_ip`. The value of this will be an object that contains the standard attributes associated with a reserved IP.
When assigning a reserved IP to a Droplet at same time as it created, the response's `links` object will contain links to both the Droplet and the assignment action. The latter can be used to check the status of the action.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2ReservedIpsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-reserved-ips-response-1.md).


# Example Usage

```csharp
ReservedIPsCreateBody body = ReservedIPsCreateBody.FromAssignToDroplet1(
    new AssignToDroplet1
    {
        DropletId = 2457247,
    }
);

try
{
    ApiResponse<V2ReservedIpsResponse1> result = await reservedIPsApi.ReservedIPsCreateAsync(body);
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


# Example Response *(as JSON)*

```json
{
  "links": {
    "actions": [
      {
        "href": "https://api.digitalocean.com/v2/actions/1088924622",
        "id": 1088924622,
        "rel": "assign_ip"
      }
    ],
    "droplets": [
      {
        "href": "https://api.digitalocean.com/v2/droplets/213939433",
        "id": 213939433,
        "rel": "droplet"
      }
    ]
  },
  "reserved_ip": {
    "droplet": null,
    "ip": "45.55.96.47",
    "locked": true,
    "project_id": "746c6152-2fa2-11ed-92d3-27aaa54e4988",
    "region": {
      "available": true,
      "features": [
        "private_networking",
        "backups",
        "ipv6",
        "metadata",
        "install_agent",
        "storage",
        "image_transfer"
      ],
      "name": "New York 3",
      "sizes": [
        "s-1vcpu-1gb",
        "s-1vcpu-2gb",
        "s-1vcpu-3gb",
        "s-2vcpu-2gb",
        "s-3vcpu-1gb",
        "s-2vcpu-4gb",
        "s-4vcpu-8gb",
        "s-6vcpu-16gb",
        "s-8vcpu-32gb",
        "s-12vcpu-48gb",
        "s-16vcpu-64gb",
        "s-20vcpu-96gb",
        "s-24vcpu-128gb",
        "s-32vcpu-192g"
      ],
      "slug": "nyc3"
    }
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



