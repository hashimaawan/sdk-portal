# Get Prometheus Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0ZSUyRk1ldHJpY3MlMkZHZXRQcm9tZXRoZXVzTWV0cmljcw

See Prometheus documentation for a complete data model.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getPrometheusMetrics(
  requestOptions?: RequestOptions
): Promise<ApiResponse<string>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: Successfully returned Prometheus metrics

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type `string`.


# Example Usage

```ts
try {
  const response = await metricsApi.getPrometheusMetrics();

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```



