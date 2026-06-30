# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

REST API interface for 1Password Connect.

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the m1PasswordConnect library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace m1PasswordConnect => ".\\Random Directory" // local path to the SDK

require m1PasswordConnect v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |
| Environment2 | - |
| Environment3 | - |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |
| loggerConfiguration | [`LoggerConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/configuration/loggerconfiguration.md) | Represents the logger configurations for API calls |
| bearerAuthCredentials | [`BearerAuthCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md) | The Credentials Setter for OAuth 2 Bearer token |

The API client can be initialized as follows:

```go
package main

import (
    "m1PasswordConnect"
)

func main() {
    client := m1PasswordConnect.NewClient(
    m1PasswordConnect.CreateConfiguration(
            m1PasswordConnect.WithHttpConfiguration(
                m1PasswordConnect.CreateHttpConfiguration(
                    m1PasswordConnect.WithTimeout(30),
                ),
            ),
            m1PasswordConnect.WithEnvironment(m1PasswordConnect.PRODUCTION),
            m1PasswordConnect.WithBearerAuthCredentials(
                m1PasswordConnect.NewBearerAuthCredentials("AccessToken"),
            ),
            m1PasswordConnect.WithLoggerConfiguration(
                m1PasswordConnect.WithLevel("info"),
                m1PasswordConnect.WithRequestConfiguration(
                    m1PasswordConnect.WithRequestBody(true),
                ),
                m1PasswordConnect.WithResponseConfiguration(
                    m1PasswordConnect.WithResponseHeaders(true),
                ),
            ),
        ),
    )
}
```


# Authorization

This API uses the following authentication schemes.

* [`ConnectToken (OAuth 2 Bearer token)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md)

## ConnectToken (OAuth 2 Bearer token)



Documentation for accessing and setting credentials for ConnectToken.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| accessToken | `string` | The OAuth 2.0 Access Token to use for API requests. | `WithAccessToken` | `AccessToken()` |



**Note:** Required auth credentials can be set using `WithBearerAuthCredentials()` by providing a credentials instance with `NewBearerAuthCredentials()` in the configuration initialization and accessed using the `BearerAuthCredentials()` method in the configuration instance.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```go
package main

import (
    "m1PasswordConnect"
)

func main() {
    client := m1PasswordConnect.NewClient(
    m1PasswordConnect.CreateConfiguration(
            m1PasswordConnect.WithBearerAuthCredentials(
                m1PasswordConnect.NewBearerAuthCredentials("AccessToken"),
            ),
        ),
    )
}
```




