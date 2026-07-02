# Droplets List Firewalls

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfbGlzdF9maXJld2FsbHM

To retrieve a list of all firewalls available to a Droplet, send a GET request
to `/v2/droplets/$DROPLET_ID/firewalls`

The response will be a JSON object that has a key called `firewalls`. This will
be set to an array of `firewall` objects, each of which contain the standard
`firewall` attributes.

```java
CompletableFuture<ApiResponse<V2DropletsFirewallsResponse>> dropletsListFirewallsAsync(
    final int dropletId,
    final Integer perPage,
    final Integer page)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `int` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |
| `perPage` | `Integer` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `Integer` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: A JSON object that has a key called `firewalls`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2DropletsFirewallsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-firewalls-response.md).


# Example Usage

```java
int dropletId = 3164444;
Integer perPage = 2;
Integer page = 1;

dropletsApi.dropletsListFirewallsAsync(dropletId, perPage, page).thenAccept(result -> {
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
  "firewalls": [
    {
      "created_at": "2020-05-23T21:24:00Z",
      "droplet_ids": [
        89989,
        33322
      ],
      "id": "bb4b2611-3d72-467b-8602-280330ecd65c",
      "inbound_rules": [
        {
          "ports": "8000-9000",
          "protocol": "udp",
          "sources": {
            "addresses": [
              "1.2.3.4",
              "18.0.0.0/8"
            ],
            "droplet_ids": [
              8282823,
              3930392
            ],
            "load_balancer_uids": [
              "4de7ac8b-495b-4884-9a69-1050c6793cd6"
            ],
            "tags": [
              "base-image",
              "dev"
            ]
          }
        }
      ],
      "name": "firewall",
      "outbound_rules": [
        {
          "destinations": {
            "addresses": [
              "1.2.3.4",
              "18.0.0.0/8"
            ],
            "droplet_ids": [
              3827493,
              213213
            ],
            "load_balancer_uids": [
              "4de7ac8b-495b-4884-9a69-1050c6793cd6"
            ],
            "tags": [
              "base-image",
              "prod"
            ]
          },
          "ports": "7000-9000",
          "protocol": "tcp"
        }
      ],
      "pending_changes": [
        {
          "droplet_id": 8043964,
          "removing": true,
          "status": "waiting"
        }
      ],
      "status": "succeeded",
      "tags": [
        "base-image",
        "prod"
      ]
    }
  ],
  "links": {
    "pages": {}
  },
  "meta": {
    "total": 1
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



