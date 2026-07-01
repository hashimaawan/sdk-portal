# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Stock and Forex Data and Realtime Quotes

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the m1ForgeFinanceApIs library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace m1ForgeFinanceApIs => ".\\Random Directory" // local path to the SDK

require m1ForgeFinanceApIs v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/go/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |
| loggerConfiguration | [`LoggerConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/go/sdk-infrastructure/configuration/loggerconfiguration.md) | Represents the logger configurations for API calls |

The API client can be initialized as follows:

```go
package main

import (
    "m1ForgeFinanceApIs"
)

func main() {
    client := m1ForgeFinanceApIs.NewClient(
    m1ForgeFinanceApIs.CreateConfiguration(
            m1ForgeFinanceApIs.WithHttpConfiguration(
                m1ForgeFinanceApIs.CreateHttpConfiguration(
                    m1ForgeFinanceApIs.WithTimeout(30),
                ),
            ),
            m1ForgeFinanceApIs.WithEnvironment(m1ForgeFinanceApIs.PRODUCTION),
            m1ForgeFinanceApIs.WithLoggerConfiguration(
                m1ForgeFinanceApIs.WithLevel("info"),
                m1ForgeFinanceApIs.WithRequestConfiguration(
                    m1ForgeFinanceApIs.WithRequestBody(true),
                ),
                m1ForgeFinanceApIs.WithResponseConfiguration(
                    m1ForgeFinanceApIs.WithResponseHeaders(true),
                ),
            ),
        ),
    )
}
```



