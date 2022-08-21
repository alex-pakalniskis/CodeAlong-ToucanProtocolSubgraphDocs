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
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| creator | User!
| owner | User!
| timestamp | BigInt!
| tx | String!
| name | String!
| startTime | BigInt!
| endTime | BigInt!
| project | Project
| batches | [BatchToken!]! @derivedFrom(field: "projectVintage")
| totalVintageQuantity | BigInt!
| isCorsiaCompliant | Boolean!
| isCCPcompliant | Boolean!
| coBenefits | String!
| correspAdjustment | String!
| additionalCertification | String!
| issuanceDate | BigInt!
| tco2Token | TCO2Token

## TCO2Token
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| creator | User!
| createdAt | BigInt!
| creationTx | String!
| projectVintage | ProjectVintage!
| name | String!
| symbol | String!
| address | String!
| score | BigInt!

## TCO2Balance
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| user | User!
| token | TCO2Token!
| balance | BigInt!

## PooledTCO2Token
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| token | TCO2Token!
| poolAddress | String!
| amount | BigInt!
  
## Retirement
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| creationTx | String!
| amount | BigInt!
| timestamp | BigInt!
| token | TCO2Token!
| creator | User!
| eventId | BigInt!
| certificate | RetirementCertificate

## RetirementCertificate
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| creationTx | String!
| updateTxs | [String!]!
| createdAt | BigInt!
| retiringEntity | User!
| beneficiary | User!
| retiringEntityString | String!
| beneficiaryString | String!
| retirementMessage | String!
| retirements | [Retirement!]! @derivedFrom(field: "certificate")

## Redeem
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| amount | BigInt!
| timestamp | BigInt!
| token | TCO2Token!
| pool | String!
| creator | User!

## Deposit
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| amount | BigInt!
| timestamp | BigInt!
| token | TCO2Token!
| pool | String!
| creator | User!

## AccessRole
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| contractAddress | String!
| role | Bytes!
| member | User!
| granted | Boolean!

## BridgeTokenRequest
| Field | Type | Description |
| --- | --- | --- | 

## ToucanToken
| Field | Type | Description |
| --- | --- | --- | 

## User
| Field | Type | Description |
| --- | --- | --- | 

## Aggregation
| Field | Type | Description |
| --- | --- | --- | 










