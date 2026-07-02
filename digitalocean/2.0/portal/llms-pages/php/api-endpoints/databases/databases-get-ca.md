# Databases Get Ca

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19nZXRfY2E

To retrieve the public certificate used to secure the connection to the database cluster send a GET request to
`/v2/databases/$DATABASE_ID/ca`.

The response will be a JSON object with a `ca` key. This will be set to an object
containing the base64 encoding of the public key certificate.

```php
function databasesGetCa(string $databaseClusterUuid): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `string` | Template, Required | A unique identifier for a database cluster. |


# Response Type

**200**: A JSON object with a key of `ca`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2DatabasesCaResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-databases-ca-response.md).


# Example Usage

```php
$databaseClusterUuid = '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30';

$databasesApi = $client->getDatabasesApi();
$apiResponse = $databasesApi->databasesGetCa($databaseClusterUuid);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2DatabasesCaResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "ca": {
    "certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUVRVENDQXFtZ0F3SUJBZ0lVRUZZWTdBWFZQS0Raam9jb1lpMk00Y0dvcU0wd0RRWUpLb1pJaHZjTkFRRU0KQlFBd09qRTRNRFlHQTFVRUF3d3ZOek0zT1RaaE1XRXRaamhrTUMwME9HSmpMV0V4Wm1NdFpqbGhNVFZsWXprdwpORGhsSUZCeWIycGxZM1FnUTBFd0hoY05NakF3TnpFM01UVTFNREEyV2hjTk16QXdOekUxTVRVMU1EQTJXakE2Ck1UZ3dOZ1lEVlFRRERDODNNemM1Tm1FeFlTMW1PR1F3TFRRNFltTXRZVEZtWXkxbU9XRXhOV1ZqT1RBME9HVWcKVUhKdmFtVmpkQ0JEUVRDQ0FhSXdEUVlKS29aSWh2Y05BUUVCQlFBRGdnR1BBRENDQVlvQ2dnR0JBTVdScXhycwpMZnpNdHZyUmxKVEw4MldYMVBLZkhKbitvYjNYcmVBY3FZd1dBUUp2Q3IycmhxSXZieVZzMGlaU0NzOHI4c3RGClljQ0R1bkxJNmUwTy9laERZYTBIT2RrMkFFRzE1ckVOVmNha2NSczcyQWlHVHNrdkNXS2VkUjFTUWswVWt0WCsKQUg4S1ExS3F5bzNtZ2Y2cVV1WUpzc3JNTXFselk3YTN1RVpEb2ZqTjN5Q3MvM21pTVJKcVcyNm1JV0IrUUlEbAo5YzdLRVF5MTZvdCtjeHVnd0lLMm9oZHMzaFY1bjBKMFVBM0I3QWRBdXY5aUl5L3JHaHlTNm5CNTdaWm9JZnAyCnFybXdOY0UrVjlIdXhQSGtRVjFOQjUwOFFudWZ4Z0E5VCtqU2VrdGVUbWFORkxqNjFXL3BtcndrTytOaWFXUTIKaGgzVXBKOEozY1BoNkErbHRnUmpSV2NEb2lsYVNwRVVpU09WemNNYVFvalZKYVJlNk9NbnZYc29NaSs3ZzdneApWcittQ0lUcGcvck9DaXpBWWQ2UFAxLzdYTjk1ZXNmU2tBQnM5c3hJakpjTUFqbDBYTEFzRmtGZVdyeHNIajlVCmJnaDNWYXdtcnpUeXhZT0RQcXV1cS9JcGlwc0RRT3Fpb2ZsUStkWEJJL3NUT0NNbVp6K0pNcG5HYXdJREFRQUIKb3o4d1BUQWRCZ05WSFE0RUZnUVVSekdDRlE3WEtUdHRDN3JzNS8ydFlQcExTZGN3RHdZRFZSMFRCQWd3QmdFQgovd0lCQURBTEJnTlZIUThFQkFNQ0FRWXdEUVlKS29aSWh2Y05BUUVNQlFBRGdnR0JBSWFKQ0dSVVNxUExtcmcvCmk3MW10b0NHUDdzeG1BVXVCek1oOEdrU25uaVdaZnZGMTRwSUtqTlkwbzVkWmpHKzZqK1VjalZtK0RIdGE1RjYKOWJPeEk5S0NFeEI1blBjRXpMWjNZYitNOTcrellxbm9zUm85S21DVFJBb2JrNTZ0WU1FS1h1aVJja2tkMm1yUQo4cGw2N2xxdThjM1V4c0dHZEZVT01wMkk3ZTNpdUdWVm5UR0ZWM3JQZUdaQ0J3WGVyUUQyY0F4UjkzS3BnWVZ2ClhUUzk5dnpSbm1HOHhhUm9EVy9FbEdXZ2xWd0Q5a1JrbXhUUkdoYTdDWVZCcjFQVWY2dVVFVjhmVFIxc1hFZnIKLytMR1JoSVVsSUhWT3l2Yzk3YnZYQURPbWF1MWZDVE5lWGtRdTNyZnZFSlBmaFlLeVIwT0V3eWVvdlhRNzl0LwpTV2ZGTjBreU1Pc1UrNVNIdHJKSEh1eWNWcU0yQlVVK083VjM1UnNwOU9MZGRZMFFVbTZldFpEVEhhSUhYYzRRCnl1Rm1OL1NhSFZtNE0wL3BTVlJQdVd6TmpxMnZyRllvSDRtbGhIZk95TUNJMjc2elE2aWhGNkdDSHlkOUJqajcKUm1UWGEyNHM3NWhmSi9YTDV2bnJSdEtpVHJlVHF6V21EOVhnUmNMQ0gyS1hJaVRtSWc9PQotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0tCg=="
  }
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



