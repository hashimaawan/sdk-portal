# Projects Patch Default

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRlByb2plY3RzJTJGcHJvamVjdHNfcGF0Y2hfZGVmYXVsdA

To update only specific attributes of your default project, send a PATCH request to `/v2/projects/default`. At least one of the following attributes needs to be sent.

```php
function projectsPatchDefault(Project $body): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/project.md) | Body, Required | - |


# Response Type

**200**: The response will be a JSON object with a key called `project`. The value of this will be an object with the standard project attributes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2ProjectsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-projects-response-1.md).


# Example Usage

```php
$body = ProjectBuilder::init()
    ->name('my-web-api')
    ->build();

$projectsApi = $client->getProjectsApi();
$apiResponse = $projectsApi->projectsPatchDefault($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2ProjectsResponse1:';
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



