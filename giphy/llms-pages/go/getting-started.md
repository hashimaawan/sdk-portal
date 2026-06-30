# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Giphy API

Official Giphy Documentation: [https://developers.giphy.com/docs/](https://developers.giphy.com/docs/)

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the giphyapi library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace giphyapi => ".\\Random Directory" // local path to the SDK

require giphyapi v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.



# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |
| customQueryAuthenticationCredentials | [`CustomQueryAuthenticationCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/getting-started/authorization.md) | The Credentials Setter for Custom Query Parameter |

The API client can be initialized as follows:

```go
package main

import (
    "giphyapi"
)

func main() {
    client := giphyapi.NewClient(
    giphyapi.CreateConfiguration(
            giphyapi.WithHttpConfiguration(
                giphyapi.CreateHttpConfiguration(
                    giphyapi.WithTimeout(0),
                ),
            ),
            giphyapi.WithCustomQueryAuthenticationCredentials(
                giphyapi.NewCustomQueryAuthenticationCredentials("api_key"),
            ),
        ),
    )
}
```


# Authorization

This API uses the following authentication schemes.

* [`api_key (Custom Query Parameter)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/getting-started/authorization.md)

## api_key (Custom Query Parameter)



Documentation for accessing and setting credentials for api_key.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| apiKey | `string` | - | `WithApiKey` | `ApiKey()` |



**Note:** Required auth credentials can be set using `WithCustomQueryAuthenticationCredentials()` by providing a credentials instance with `NewCustomQueryAuthenticationCredentials()` in the configuration initialization and accessed using the `CustomQueryAuthenticationCredentials()` method in the configuration instance.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```go
package main

import (
    "giphyapi"
)

func main() {
    client := giphyapi.NewClient(
    giphyapi.CreateConfiguration(
            giphyapi.WithCustomQueryAuthenticationCredentials(
                giphyapi.NewCustomQueryAuthenticationCredentials("api_key"),
            ),
        ),
    )
}
```


# Test the SDK

`Go Testing` is used as the testing framework. To run the unit tests of the SDK, navigate to the root directory of the SDK and run the following command in the terminal:

```bash
$ go test
```



