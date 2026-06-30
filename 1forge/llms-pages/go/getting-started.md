# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Stock and Forex Data and Realtime Quotes

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the m1forgefinanceapis library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace m1forgefinanceapis => ".\\Random Directory" // local path to the SDK

require m1forgefinanceapis v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/llms-pages/go/getting-started/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |

The API client can be initialized as follows:

```go
package main

import (
    "m1forgefinanceapis"
)

func main() {
    client := m1forgefinanceapis.NewClient(
    m1forgefinanceapis.CreateConfiguration(
            m1forgefinanceapis.WithHttpConfiguration(
                m1forgefinanceapis.CreateHttpConfiguration(
                    m1forgefinanceapis.WithTimeout(0),
                ),
            ),
            m1forgefinanceapis.WithEnvironment(m1forgefinanceapis.PRODUCTION),
        ),
    )
}
```



