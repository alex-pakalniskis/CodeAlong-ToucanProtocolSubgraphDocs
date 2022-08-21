# CodeAlong-ToucanProtocolSubgraphDocs

## Resources
Toucan Protocol Docs
* [Toucan Protocol Subgraph Manifest](https://ipfs.io/ipfs/Qmbzn47G3NBgHuDyFqXaf646SCRz2CK93VBkUD3AV7nGtk)
* [Protocol Summary - Toucan Protocol Docs](https://docs.toucan.earth/protocol/introduction/overview)

Reference Subgraph Docs
* [Juicebox Subgraph docs](https://info.juicebox.money/dev/subgraph/)
* [Connext Subgraph docs](https://docs.connext.network/developers/subgraph/SubgraphData)
* [Sablier Docs](https://docs.sablier.finance/protocol/subgraph/endpoints)

The Graph Docs
* [The Subgraph Manifest - Creating a Subgraph - The Graph Docs](https://thegraph.com/docs/en/developing/creating-a-subgraph/#the-subgraph-manifest)

## Subgraph Documentation Components
### Overview
* Sabilier
  * Sablier has a GraphQL API Endpoint hosted by The Graph called a subgraph for indexing and organizing data from the Sablier smart contracts. The code repository for our subgraph can be found here.
  * Official subgraphs are subgraphs maintained by the Sablier team.
  * Unofficial subgraphs are subgraphs maintained by external teams.
* Connext
  * Connext has a GraphQL API Endpoint hosted by The Graph called a subgraph for indexing and organizing data from the Connext smart contracts.
  * This subgraph is can be used to query Connext bridge transactions, transactions statuses and more.
  * Subgraph information is serviced by a decentralized group of server operators called Indexers - and thus our decentralized application also has decentralized data endpoints.
* Juicebox
  * juicebox.money uses The Graph to load data from Juicebox protocol contracts without directly querying the blockchain.
  * Multiple subgraphs are maintained by Peel in a Graph Studio owned by the Peel Gnosis safe. Only the primary Juicebox subgraph has been published to the Graph Network; others are available to use for free with rate-limited queries.
  * The Juicebox subgraph schema is the same on all networks, and can be found on the following page. For information on structuring Graph queries, read the Graph docs. You can also reference the tools used for juicebox.money.

### Subgraph Entities
Sablier
* [Subgraph entities](https://docs.sablier.finance/protocol/subgraph/entities)
* [Subgraph schema.graphql](https://github.com/sablierhq/subgraph/blob/main/schema.graphql)

Connext
* [Subgraph entities](https://docs.connext.network/developers/subgraph/Entities)
* [Subgraph schema.graphql](https://github.com/connext/nxtp/blob/56a166f3ecb50cc10356dd96c257e2e4d47f29e3/packages/deployments/subgraph/src/amarok-runtime-v0/schema.graphql)

Juicebox
* [Subgraph entities](https://info.juicebox.money/dev/subgraph/entities)
* [Subgraph schema.graphql](https://github.com/jbx-protocol/juice-subgraph/blob/main/schema.graphql)

### Sample Queries
Sablier
* [Sample queries](https://docs.sablier.finance/protocol/subgraph/queries)
  * Sender Streams
  * Receiver Streams

Connext
* [Sample queries](https://docs.connext.network/developers/subgraph/Queries)
  * Get Asset Balances for Router
  * Get Account's Most Recent Prepared Transaction

Juicebox
* [Sample queries](https://info.juicebox.money/dev/subgraph/queries)
  * Get Project Metrics By Owner
  * Project Metrics
  * Project Payments



