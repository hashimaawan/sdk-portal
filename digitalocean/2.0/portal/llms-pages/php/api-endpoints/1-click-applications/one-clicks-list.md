# One Clicks List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRjEtQ2xpY2slMjUyMEFwcGxpY2F0aW9ucyUyRm9uZUNsaWNrc19saXN0

To list all available 1-Click applications, send a GET request to `/v2/1-clicks`. The `type` may
be provided as query paramater in order to restrict results to a certain type of 1-Click, for
example: `/v2/1-clicks?type=droplet`. Current supported types are `kubernetes` and `droplet`.

The response will be a JSON object with a key called `1_clicks`. This will be set to an array of
1-Click application data, each of which will contain the the slug and type for the 1-Click.

```php
function oneClicksList(?string $type = null): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`?string(Type)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type.md) | Query, Optional | Restrict results to a certain type of 1-Click. |


# Response Type

**200**: A JSON object with a key of `1_clicks`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V21ClicksResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-1-clicks-response.md).


# Example Usage

```php
$type = Type::KUBERNETES;

$m1ClickApplicationsApi = $client->getM1ClickApplicationsApi();
$apiResponse = $m1ClickApplicationsApi->oneClicksList($type);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V21ClicksResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "1_clicks": [
    {
      "slug": "monitoring",
      "type": "kubernetes"
    },
    {
      "slug": "wordpress-18-04",
      "type": "droplet"
    }
  ]
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



