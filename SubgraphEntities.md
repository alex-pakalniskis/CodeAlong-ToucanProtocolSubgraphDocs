# Subgraph Entities

## Entities

* [BatchToken](#batchtoken)
* [BatchComment](#batchcomment)
* [Project](#project)
* [ProjectVintage](#projectvintage)
* [TCO2Token](#tco2token)
* [TCO2Balance](#tco2balance)
* [PooledTCO2Token](#pooledtco2token)
* [Retirement](#retirement)
* [RetirementCertificate](#retirementcertificate)
* [Redeem](#redeem)
* [Deposit](#deposit)
* [AccessRole](#accessrole)
* [BridgeTokenRequest](#bridgetokenrequest)
* [ToucanToken](#toucantoken)
* [User](#user)
* [Aggregation](#aggregation)

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
| comments | [BatchComment!](#batchcomment) | | 
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
| vintages | [ProjectVintage!](#projectvintage)
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
| batches | [BatchToken!](#batchtoken)
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
| retirements | [Retirement!](#retirement)

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
| id | ID!
| sentTx | String
| sentTimestamp | BigInt
| receivedTx | String
| receivedTimestamp | BigInt
| originDomain | BigInt!
| toDomain | BigInt!
| sentToken | ToucanToken
| receivedToken | ToucanToken
| bridger | User!
| amount | BigInt!
| requesthash | Bytes!

## ToucanToken
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| name | String!
| symbol | String!
| address | String!
| decimals | Int!

## User
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| batchesOwned | [BatchToken!](#batchtoken)
| batchesCreated | [BatchToken!](#batchtoken)
| batchComments | [BatchComment!](#batchcomment)
| projectsOwned | [Project!](#project)
| projectsCreated | [Project!](#project)
| vintagesOwned | [ProjectVintage!](#projectvintage)
| vintagesCreated | [ProjectVintage!](#projectvintage)
| retirementsCreated | [Retirement!](#retirement)
| redeemsCreated | [Redeem!](#redeem)
| tokensOwned | [TCO2Balance!](#tco2balance)
| bridgeRequestOwned | [BridgeTokenRequest!](#bridgetokenrequest)

## Aggregation
| Field | Type | Description |
| --- | --- | --- | 
| id | ID!
| key | String!
| value | BigInt!









