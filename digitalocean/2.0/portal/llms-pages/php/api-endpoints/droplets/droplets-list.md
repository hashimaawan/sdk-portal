# Droplets List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfbGlzdA

To list all Droplets in your account, send a GET request to `/v2/droplets`.

The response body will be a JSON object with a key of `droplets`. This will be
set to an array containing objects each representing a Droplet. These will
contain the standard Droplet attributes.

### Filtering Results by Tag

It's possible to request filtered results by including certain query parameters.
To only list Droplets assigned to a specific tag, include the `tag_name` query
parameter set to the name of the tag in your GET request. For example,
`/v2/droplets?tag_name=$TAG_NAME`.

```php
function dropletsList(
    ?int $perPage = 20,
    ?int $page = 1,
    ?string $tagName = null,
    ?string $name = null
): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perPage` | `?int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `?int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `tagName` | `?string` | Query, Optional | Used to filter Droplets by a specific tag. Can not be combined with `name`. |
| `name` | `?string` | Query, Optional | Used to filter list response by Droplet name returning only exact matches. It is case-insensitive and can not be combined with `tag_name`. |


# Response Type

**200**: A JSON object with a key of `droplets`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2DropletsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-response.md).


# Example Usage

```php
$perPage = 2;

$page = 1;

$tagName = 'env:prod';

$name = 'web-01';

$dropletsApi = $client->getDropletsApi();
$apiResponse = $dropletsApi->dropletsList(
    $perPage,
    $page,
    $tagName,
    $name
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2DropletsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "droplets": [
    {
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
    },
    {
      "backup_ids": [],
      "created_at": "2020-07-21T18:42:27Z",
      "disk": 25,
      "features": [
        "private_networking"
      ],
      "id": 3164459,
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
      "name": "assets.example.com",
      "networks": {
        "v4": [
          {
            "gateway": "nil",
            "ip_address": "10.128.192.138",
            "netmask": "255.255.0.0",
            "type": "private"
          },
          {
            "gateway": "162.243.0.1",
            "ip_address": "162.243.0.4",
            "netmask": "255.255.255.0",
            "type": "public"
          }
        ],
        "v6": []
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
      "snapshot_ids": [],
      "status": "active",
      "tags": [
        "storage",
        "env:prod"
      ],
      "vcpus": 1,
      "volume_ids": [
        "506f78a4-e098-11e5-ad9f-000f53306ae1"
      ],
      "vpc_uuid": "760e09ef-dc84-11e8-981e-3cfdfeaae000"
    },
    {
      "backup_ids": [],
      "created_at": "2020-07-21T18:32:55Z",
      "disk": 25,
      "features": [
        "private_networking"
      ],
      "id": 3164412,
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
      "name": "stage.example.com",
      "networks": {
        "v4": [
          {
            "gateway": "nil",
            "ip_address": "10.128.192.125",
            "netmask": "255.255.0.0",
            "type": "private"
          },
          {
            "gateway": "192.241.247.1",
            "ip_address": "192.241.247.248",
            "netmask": "255.255.255.0",
            "type": "public"
          }
        ],
        "v6": []
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
      "snapshot_ids": [],
      "status": "active",
      "tags": [
        "env:stage"
      ],
      "vcpus": 1,
      "volume_ids": [
        "7724db7c-e098-11e5-b522-000f53304e51"
      ],
      "vpc_uuid": "5a4981aa-9653-4bd1-bef5-d6bff52042e4"
    }
  ],
  "links": {
    "pages": {}
  },
  "meta": {
    "total": 3
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



