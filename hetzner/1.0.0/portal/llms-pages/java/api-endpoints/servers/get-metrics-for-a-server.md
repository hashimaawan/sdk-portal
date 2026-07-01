# Get Metrics for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyME1ldHJpY3MlMjUyMGZvciUyNTIwYSUyNTIwU2VydmVy

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

```java
CompletableFuture<ServersMetricsResponse> getMetricsForAServerAsync(
    final int id,
    final Type66Enum type,
    final String start,
    final String end,
    final String step)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `type` | [`Type66Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-66.md) | Query, Required | Type of metrics to get |
| `start` | `String` | Query, Required | Start of period to get Metrics for (in ISO-8601 format) |
| `end` | `String` | Query, Required | End of period to get Metrics for (in ISO-8601 format) |
| `step` | `String` | Query, Optional | Resolution of results in seconds |


# Response Type

**200**: The `metrics` key in the reply contains a metrics object with this structure

[`ServersMetricsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/servers-metrics-response.md)


# Example Usage

```java
int id = 112;
Type66Enum type = Type66Enum.NETWORK;
String start = "start4";
String end = "end8";

serversController.getMetricsForAServerAsync(id, type, start, end, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



