# Registry Run Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkNvbnRhaW5lciUyNTIwUmVnaXN0cnklMkZyZWdpc3RyeV9ydW5fZ2FyYmFnZUNvbGxlY3Rpb24

Garbage collection enables users to clear out unreferenced blobs (layer &
manifest data) after deleting one or more manifests from a repository. If
there are no unreferenced blobs resulting from the deletion of one or more
manifests, garbage collection is effectively a noop.
[See here for more information](https://www.digitalocean.com/docs/container-registry/how-to/clean-up-container-registry/)
about how and why you should clean up your container registry periodically.

To request a garbage collection run on your registry, send a POST request to
`/v2/registry/$REGISTRY_NAME/garbage-collection`. This will initiate the
following sequence of events on your registry.

* Set the registry to read-only mode, meaning no further write-scoped
  JWTs will be issued to registry clients. Existing write-scoped JWTs will
  continue to work until they expire which can take up to 15 minutes.
* Wait until all existing write-scoped JWTs have expired.
* Scan all registry manifests to determine which blobs are unreferenced.
* Delete all unreferenced blobs from the registry.
* Record the number of blobs deleted and bytes freed, mark the garbage
  collection status as `success`.
* Remove the read-only mode restriction from the registry, meaning write-scoped
  JWTs will once again be issued to registry clients.

```php
function registryRunGarbageCollection(string $registryName): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `registryName` | `string` | Template, Required | The name of a container registry. |


# Response Type

**201**: The response will be a JSON object with a key of `garbage_collection`. This will be a json object with attributes representing the currently-active garbage collection.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2RegistryGarbageCollectionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-registry-garbage-collection-response.md).


# Example Usage

```php
$registryName = 'example';

$containerRegistryApi = $client->getContainerRegistryApi();
$apiResponse = $containerRegistryApi->registryRunGarbageCollection($registryName);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2RegistryGarbageCollectionResponse:';
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



