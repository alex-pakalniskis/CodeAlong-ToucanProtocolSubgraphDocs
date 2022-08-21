# Subgraph Entities

## Entities

* BatchToken
* BatchComment
* Project
* ProjectVintage
* TCO2Token
* TCO2Balance
* PooledTCO2Token
* Retirement
* RetirementCertificate
* Redeem
* Deposit
* AccessRole
* BridgeTokenRequest
* ToucanToken
* User
* Aggregation

## BatchToken
| Field | Type | Description | 
| --- | --- | --- | 
| id | ID! | |
| creator | User! | 
| owner | User! | | 
| projectVintage | ProjectVintage | | 
| serialNumber | String | |
| quantity | BigInt | |
| confirmationStatus | Int! | |
| timestamp | BigInt! | |
| tx | String! | | 
| contentURI | String | | 
| comments | [BatchComment!]! @derivedFrom(field: "batch") | | 
| aggregated | Boolean | | 


## BatchComment
| Field | Type | Description | 
| --- | --- | --- |
| id | ID! | | 
| sender | User | | 
| batch | BatchToken! | |
| comment | String! | |

## Project
| Field | Type | Description |
| --- | --- | --- | 
| id | ID! | | 
| creator | User!
| owner | User!
| timestamp | BigInt!
| tx | String!
| projectId | String!
| vintages | [ProjectVintage!]! @derivedFrom(field: "project")
| standard | String!
| methodology  |String
| region | String
| storageMethod | String
| method | String
| emissionType | String
| category | String
| uri | String

## ProjectVintage

## TCO2Token

## TCO2Balance

## PooledTCO2Token

## Retirement

## RetirementCertificate

## Redeem

## Deposit

## AccessRole

## BridgeTokenRequest

## ToucanToken

## User

## Aggregation










