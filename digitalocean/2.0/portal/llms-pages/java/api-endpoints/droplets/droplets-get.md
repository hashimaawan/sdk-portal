# Droplets Get

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfZ2V0

To show information about an individual Droplet, send a GET request to
`/v2/droplets/$DROPLET_ID`.

```java
CompletableFuture<ApiResponse<V2DropletsResponse1>> dropletsGetAsync(
    final int dropletId)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `int` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: The response will be a JSON object with a key called `droplet`. This will be
set to a JSON object that contains the standard Droplet attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2DropletsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-response-1.md).


# Example Usage

```java
int dropletId = 3164444;

dropletsApi.dropletsGetAsync(dropletId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```


# Example Response *(as JSON)*

```json
{
  "droplet": {
    "backup_ids": [
      53893572
    ],
    "created_at": "2020-07-21T18:37:44Z",
    "disk": 25,
    "features": [
      "backups",
      "private_networking",
      "ipv6"
    ],
    "id": 3164444,
    "image": {
      "created_at": "2020-05-15T05:47:50Z",
      "description": "",
      "distribution": "Ubuntu",
      "error_message": "",
      "id": 63663980,
      "min_disk_size": 20,
      "name": "20.04 (LTS) x64",
      "public": true,
      "regions": [
        "ams2",
        "ams3",
        "blr1",
        "fra1",
        "lon1",
        "nyc1",
        "nyc2",
        "nyc3",
        "sfo1",
        "sfo2",
        "sfo3",
        "sgp1",
        "tor1"
      ],
      "size_gigabytes": 2.36,
      "slug": "ubuntu-20-04-x64",
      "status": "available",
      "tags": [],
      "type": "snapshot"
    },
    "kernel": null,
    "locked": false,
    "memory": 1024,
    "name": "example.com",
    "networks": {
      "v4": [
        {
          "gateway": "nil",
          "ip_address": "10.128.192.124",
          "netmask": "255.255.0.0",
          "type": "private"
        },
        {
          "gateway": "192.241.165.1",
          "ip_address": "192.241.165.154",
          "netmask": "255.255.255.0",
          "type": "public"
        }
      ],
      "v6": [
        {
          "gateway": "2604:a880:0:1010::1",
          "ip_address": "2604:a880:0:1010::18a:a001",
          "netmask": 64,
          "type": "public"
        }
      ]
    },
    "next_backup_window": {
      "end": "2020-07-30T23:00:00Z",
      "start": "2020-07-30T00:00:00Z"
    },
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
    },
    "size": {
      "available": true,
      "description": "Basic",
      "disk": 25,
      "memory": 1024,
      "price_hourly": 0.00743999984115362,
      "price_monthly": 5,
      "regions": [
        "ams2",
        "ams3",
        "blr1",
        "fra1",
        "lon1",
        "nyc1",
        "nyc2",
        "nyc3",
        "sfo1",
        "sfo2",
        "sfo3",
        "sgp1",
        "tor1"
      ],
      "slug": "s-1vcpu-1gb",
      "transfer": 1,
      "vcpus": 1
    },
    "size_slug": "s-1vcpu-1gb",
    "snapshot_ids": [
      67512819
    ],
    "status": "active",
    "tags": [
      "web",
      "env:prod"
    ],
    "vcpus": 1,
    "volume_ids": [],
    "vpc_uuid": "760e09ef-dc84-11e8-981e-3cfdfeaae000"
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



