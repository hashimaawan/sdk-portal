# Get Metrics for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyME1ldHJpY3MlMjUyMGZvciUyNTIwYSUyNTIwU2VydmVy

Get Metrics for specified Server.

You must specify the type of metric to get: cpu, disk or network. You can also specify more than one type by comma separation, e.g. cpu,disk.

Depending on the type you will get different time series data

| Type    | Timeseries              | Unit      | Description                                          |
|---------|-------------------------|-----------|------------------------------------------------------|
| cpu     | cpu                     | percent   | Percent CPU usage                                    |
| disk    | disk.0.iops.read        | iop/s     | Number of read IO operations per second              |
|         | disk.0.iops.write       | iop/s     | Number of write IO operations per second             |
|         | disk.0.bandwidth.read   | bytes/s   | Bytes read per second                                |
|         | disk.0.bandwidth.write  | bytes/s   | Bytes written per second                             |
| network | network.0.pps.in        | packets/s | Public Network interface packets per second received |
|         | network.0.pps.out       | packets/s | Public Network interface packets per second sent     |
|         | network.0.bandwidth.in  | bytes/s   | Public Network interface bytes/s received            |
|         | network.0.bandwidth.out | bytes/s   | Public Network interface bytes/s sent                |

Metrics are available for the last 30 days only.

If you do not provide the step argument we will automatically adjust it so that a maximum of 200 samples are returned.

We limit the number of samples returned to a maximum of 500 and will adjust the step parameter accordingly.

:information_source: **Note** This endpoint does not require authentication.

```php
function getMetricsForAServer(
    int $id,
    string $type,
    string $start,
    string $end,
    ?string $step = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `type` | [`string(Type66)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-66.md) | Query, Required | Type of metrics to get |
| `start` | `string` | Query, Required | Start of period to get Metrics for (in ISO-8601 format) |
| `end` | `string` | Query, Required | End of period to get Metrics for (in ISO-8601 format) |
| `step` | `?string` | Query, Optional | Resolution of results in seconds |


# Response Type

**200**: The `metrics` key in the reply contains a metrics object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ServersMetricsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/servers-metrics-response.md).


# Example Usage

```php
$id = 112;

$type = Type66::NETWORK;

$start = 'start4';

$end = 'end8';

$serversApi = $client->getServersApi();
$apiResponse = $serversApi->getMetricsForAServer(
    $id,
    $type,
    $start,
    $end
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ServersMetricsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



