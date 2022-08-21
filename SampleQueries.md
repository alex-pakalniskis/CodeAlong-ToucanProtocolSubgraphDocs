---
sidebar_position: 3
title: Sample Queries
---

## Sample Queries

Below are some sample queries you can use to gather information from the Toucan contracts.

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit your queries to the exact data desired.

### Get Single Vintage

Get information on a signle vintage

```graphql
{
  projectVintages(where: {id: "366"}) {
    totalVintageQuantity
    startTime
    name
    project {
      id
      projectId
      region
      methodology
    }
    tco2Token {
      id
    }
  }
}
```

### Get Single Batch Token

```graphql
{
  batchTokens(where: {id: "536"}) {
    id
    confirmationStatus
    owner {
      id
    }
    projectVintage {
      id
      totalVintageQuantity
      startTime
      project {
        id
        projectId
      }
      tco2Token {
        id
      }
    }
    tx
    serialNumber
    quantity
  }
}
```

### BCT Contents
```graphql
{
  pooledTCO2Tokens(
    where: {poolAddress: "0x2f800db0fdb5223b3c3f354886d907a671414a7f"}
  ) {
    token {
      name
      projectVintage {
        id
        project {
          methodology
          standard
        }
      }
    }
    amount
  }
}
```
