# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

<p>Amazon Athena is an interactive query service that lets you use standard SQL to analyze data directly in Amazon S3. You can point Athena at your data in Amazon S3 and run ad-hoc queries and get results in seconds. Athena is serverless, so there is no infrastructure to set up or manage. You pay only for the queries you run. Athena scales automatically—executing queries in parallel—so results are fast, even with large datasets and complex queries. For more information, see <a href="http://docs.aws.amazon.com/athena/latest/ug/what-is.html">What is Amazon Athena</a> in the <i>Amazon Athena User Guide</i>.</p> <p>If you connect to Athena using the JDBC driver, use version 1.1.0 of the driver or later with the Amazon Athena API. Earlier version drivers do not support the API. For more information and to download the driver, see <a href="https://docs.aws.amazon.com/athena/latest/ug/connect-with-jdbc.html">Accessing Amazon Athena with JDBC</a>.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="https://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


Amazon Web Services documentation: [https://docs.aws.amazon.com/athena/](https://docs.aws.amazon.com/athena/)

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the amazonathena library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace amazonathena => ".\\Random Directory" // local path to the SDK

require amazonathena v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** The Amazon Athena multi-region endpoint |
| ENVIRONMENT2 | The Amazon Athena multi-region endpoint |
| ENVIRONMENT3 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |
| ENVIRONMENT4 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| region | `models.RegionEnum` | The AWS region<br>*Default*: `"us-east-1"` |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |
| customHeaderAuthenticationCredentials | [`CustomHeaderAuthenticationCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md) | The Credentials Setter for Custom Header Signature |

The API client can be initialized as follows:

```go
package main

import (
    "amazonathena"
)

func main() {
    client := amazonathena.NewClient(
    amazonathena.CreateConfiguration(
            amazonathena.WithHttpConfiguration(
                amazonathena.CreateHttpConfiguration(
                    amazonathena.WithTimeout(0),
                ),
            ),
            amazonathena.WithEnvironment(amazonathena.PRODUCTION),
            amazonathena.WithCustomHeaderAuthenticationCredentials(
                amazonathena.NewCustomHeaderAuthenticationCredentials("Authorization"),
            ),
            amazonathena.WithRegion("us-east-1"),
        ),
    )
}
```


# Authorization

This API uses the following authentication schemes.

* [`hmac (Custom Header Signature)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)

## hmac (Custom Header Signature)



Documentation for accessing and setting credentials for hmac.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| authorization | `string` | Amazon Signature authorization v4 | `WithAuthorization` | `Authorization()` |



**Note:** Required auth credentials can be set using `WithCustomHeaderAuthenticationCredentials()` by providing a credentials instance with `NewCustomHeaderAuthenticationCredentials()` in the configuration initialization and accessed using the `CustomHeaderAuthenticationCredentials()` method in the configuration instance.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```go
package main

import (
    "amazonathena"
)

func main() {
    client := amazonathena.NewClient(
    amazonathena.CreateConfiguration(
            amazonathena.WithCustomHeaderAuthenticationCredentials(
                amazonathena.NewCustomHeaderAuthenticationCredentials("Authorization"),
            ),
        ),
    )
}
```




