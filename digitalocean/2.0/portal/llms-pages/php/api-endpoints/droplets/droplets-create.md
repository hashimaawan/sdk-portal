# Droplets Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfY3JlYXRl

To create a new Droplet, send a POST request to `/v2/droplets` setting the
required attributes.

A Droplet will be created using the provided information. The response body
will contain a JSON object with a key called `droplet`. The value will be an
object containing the standard attributes for your new Droplet. The response
code, 202 Accepted, does not indicate the success or failure of the operation,
just that the request has been accepted for processing. The `actions` returned
as part of the response's `links` object can be used to check the status
of the Droplet create event.

### Create Multiple Droplets

Creating multiple Droplets is very similar to creating a single Droplet.
Instead of sending `name` as a string, send `names` as an array of strings. A
Droplet will be created for each name you send using the associated
information. Up to ten Droplets may be created this way at a time.

Rather than returning a single Droplet, the response body will contain a JSON
array with a key called `droplets`. This will be set to an array of JSON
objects, each of which will contain the standard Droplet attributes. The
response code, 202 Accepted, does not indicate the success or failure of any
operation, just that the request has been accepted for processing. The array
of `actions` returned as part of the response's `links` object can be used to
check the status of each individual Droplet create event.

```php
function dropletsCreate($body = null): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [SingleDropletRequest](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/single-droplet-request.md)\|[MultipleDropletRequest](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/multiple-droplet-request.md)\|null | Body, Optional | This is a container for one-of cases. |


# Response Type

**202**: Accepted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type `SingleDropletResponse|MultipleDropletResponse`.


# Example Usage

```php
$body = MultipleDropletRequestBuilder::init(
    [
        'sub-01.example.com',
        'sub-02.example.com'
    ],
    'ubuntu-20-04-x64',
    's-1vcpu-1gb'
)
    ->backups(true)
    ->ipv6(true)
    ->monitoring(true)
    ->region('nyc3')
    ->sshKeys(
        [
            289794,
            '3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45'
        ]
    )
    ->tags(
        [
            'env:prod',
            'web'
        ]
    )
    ->userData('#cloud-config
runcmd:
  - touch /test.txt
')
    ->vpcUuid('760e09ef-dc84-11e8-981e-3cfdfeaae000')
    ->build();

$dropletsApi = $client->getDropletsApi();
$apiResponse = $dropletsApi->dropletsCreate($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'SingleDropletResponse|MultipleDropletResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response

```
{
  "droplets": [
    {
      "backup_ids": [],
      "created_at": "2020-07-21T18:37:44Z",
      "disk": 25,
      "features": [
        "backups",
        "private_networking",
        "ipv6",
        "monitoring"
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
      "name": "sub-01.example.com",
      "networks": {
        "v4": [],
        "v6": []
      },
      "next_backup_window": null,
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
      "status": "new",
      "tags": [
        "web",
        "env:prod"
      ],
      "vcpus": 1,
      "volume_ids": []
    },
    {
      "backup_ids": [],
      "created_at": "2020-07-21T18:37:44Z",
      "disk": 25,
      "features": [
        "backups",
        "private_networking",
        "ipv6",
        "monitoring"
      ],
      "id": 3164445,
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
      "name": "sub-02.example.com",
      "networks": {
        "v4": [],
        "v6": []
      },
      "next_backup_window": null,
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
      "status": "new",
      "tags": [
        "web",
        "env:prod"
      ],
      "vcpus": 1,
      "volume_ids": []
    }
  ],
  "links": {
    "actions": [
      {
        "href": "https://api.digitalocean.com/v2/actions/7515",
        "id": 7515,
        "rel": "create"
      },
      {
        "href": "https://api.digitalocean.com/v2/actions/7516",
        "id": 7516,
        "rel": "create"
      }
    ]
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



