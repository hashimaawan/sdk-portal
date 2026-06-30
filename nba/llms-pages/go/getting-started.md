# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

The destination for current and historic NBA statistics.

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the nbastatsapi library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace nbastatsapi => ".\\Random Directory" // local path to the SDK

require nbastatsapi v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.



# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |

The API client can be initialized as follows:

```go
package main

import (
    "nbastatsapi"
)

func main() {
    client := nbastatsapi.NewClient(
    nbastatsapi.CreateConfiguration(
            nbastatsapi.WithHttpConfiguration(
                nbastatsapi.CreateHttpConfiguration(
                    nbastatsapi.WithTimeout(0),
                ),
            ),
        ),
    )
}
```



