# Uptime Alert Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRlVwdGltZSUyRnVwdGltZV9hbGVydF9jcmVhdGU

To create an Uptime alert, send a POST request to `/v2/uptime/checks/$CHECK_ID/alerts` specifying the attributes
in the table below in the JSON body.

```php
function uptimeAlertCreate(string $checkId, Alerts1 $body): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkId` | `string` | Template, Required | A unique identifier for a check. |
| `body` | [`Alerts1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/alerts-1.md) | Body, Required | The ''type'' field dictates the type of alert, and hence what type of value to pass into the threshold property.<br>Type \| Description \| Threshold Value<br>-----\|-------------\|--------------------<br>`latency` \| alerts on the response latency \| milliseconds<br>`down` \| alerts on a target registering as down in any region \| N/A (Not required)<br>`down_global` \| alerts on a target registering as down globally \| N/A (Not required)<br>`ssl_expiry` \| alerts on a SSL certificate expiring within $threshold days \| days |


# Response Type

**201**: The response will be a JSON object with a key called `alert`. The value of this will be an object that contains the standard attributes associated with an uptime alert.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2UptimeChecksAlertsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-uptime-checks-alerts-response-1.md).


# Example Usage

```php
$checkId = '4de7ac8b-495b-4884-9a69-1050c6793cd6';

$body = Alerts1Builder::init()
    ->comparison(Comparison::GREATER_THAN)
    ->name('Landing page degraded performance')
    ->period(Period::ENUM_2M)
    ->threshold(300)
    ->type(Type20::LATENCY)
    ->build();

$uptimeApi = $client->getUptimeApi();
$apiResponse = $uptimeApi->uptimeAlertCreate(
    $checkId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2UptimeChecksAlertsResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



