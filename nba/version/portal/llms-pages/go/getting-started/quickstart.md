# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

The destination for current and historic NBA statistics.

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the nbaStatsApi library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace nbaStatsApi => ".\\Random Directory" // local path to the SDK

require nbaStatsApi v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.



# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |
| loggerConfiguration | [`LoggerConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/configuration/loggerconfiguration.md) | Represents the logger configurations for API calls |

The API client can be initialized as follows:

```go
package main

import (
    "nbaStatsApi"
)

func main() {
    client := nbaStatsApi.NewClient(
    nbaStatsApi.CreateConfiguration(
            nbaStatsApi.WithHttpConfiguration(
                nbaStatsApi.CreateHttpConfiguration(
                    nbaStatsApi.WithTimeout(30),
                ),
            ),
            nbaStatsApi.WithLoggerConfiguration(
                nbaStatsApi.WithLevel("info"),
                nbaStatsApi.WithRequestConfiguration(
                    nbaStatsApi.WithRequestBody(true),
                ),
                nbaStatsApi.WithResponseConfiguration(
                    nbaStatsApi.WithResponseHeaders(true),
                ),
            ),
        ),
    )
}
```



