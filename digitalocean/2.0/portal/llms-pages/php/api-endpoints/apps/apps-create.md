# Apps Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NyZWF0ZQ

Create a new app by submitting an app specification. For documentation on app specifications (`AppSpec` objects), please refer to [the product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/).

```php
function appsCreate(V2AppsRequest $body, ?string $accept = null, ?string $contentType = null): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2AppsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-apps-request.md) | Body, Required | - |
| `accept` | [`?string(Accept)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/accept.md) | Header, Optional | The content-type that should be used by the response. By default, the response will be `application/json`. `application/yaml` is also supported. |
| `contentType` | [`?string(ContentType)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/content-type.md) | Header, Optional | The content-type used for the request. By default, the requests are assumed to use `application/json`. `application/yaml` is also supported. |


# Response Type

**200**: A JSON or YAML of a `spec` object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2AppsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-apps-response-1.md).


# Example Usage

```php
$body = V2AppsRequestBuilder::init(
    AppSpecBuilder::init(
        'web-app'
    )
        ->region(Region1::NYC)
        ->services(
            [
                ServiceBuilder::init(
                    'api'
                )
                    ->environmentSlug('node-js')
                    ->github(
                        GithubBuilder::init()
                            ->branch('main')
                            ->deployOnPush(true)
                            ->repo('digitalocean/sample-golang')
                            ->build()
                    )
                    ->runCommand('bin/api')
                    ->instanceCount(2)
                    ->instanceSizeSlug(InstanceSizeSlug::BASICXXS)
                    ->routes(
                        [
                            ACriterionForRoutingHttpTrafficToAComponentBuilder::init()
                                ->path('/api')
                                ->build()
                        ]
                    )
                    ->build()
            ]
        )
        ->build()
)->build();

$accept = Accept::ENUM_APPLICATIONJSON;

$contentType = ContentType::ENUM_APPLICATIONJSON;

$appsApi = $client->getAppsApi();
$apiResponse = $appsApi->appsCreate(
    $body,
    $accept,
    $contentType
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2AppsResponse1:';
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



