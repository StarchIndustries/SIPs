---
SIP: 819
Title: Minimization of API Calls for Blockchain Submissions
Status: Pending
Category: API
Authors:
  - Huth S0lo <john@themorphium.io>
Implementors: N/A
Discussions:
  - None so far...
Created: 2024-01-19
License: CC-BY-4.0
---

## Abstract

Improvement of existing API endpoints to minimize necessary API interaction for block submission.

## Motivation

To submit new candidate blocks to the Starch Blockchain, a miner must pull a copy of the latest blockchain information, calculate a new block for itself, and then submit this calculated block to be considered as a candidate for the next block on the blockchain.  The current API design is to submit one block at a time.  If a user or oganization owns more than one miner, they must make multiple API calls to submit their blocks.  Along with the added strain to the API for these additional submissions, the API is restricted to 10 calls per minute; creating potential rate limiting scenarios,  

## Specification

A new API Endpoint shall be created, that can accept an array of blocks, in addition to the current API Endpoint for a single block

### Current API Endpoint for Blockchain Submission Design

Endpoint: /api/submit_block

Payload Format: {"hash": new_hash, "color": color, "miner_id": miner_id}

### Proposed new API Endpoint for Multiple Block Submissions

/api/submit_blocks or /api/submit_multi

Payload Format: [{"hash": new_hash, "color": color, "miner_id": miner_id_1}, {"hash": new_hash, "color": color, "miner_id": miner_id_2}, {"hash": new_hash, "color": color, "miner_id": miner_id_3}, ...] 

#### Anecdotal Feedback

To balance the minimization of API calls along with the intention of decentralization, a maximum number of submissions should be implemented based on community consensus.  This proposal recommends a limit of 5, and preferentially be restricted by IP Address.

### Editors

| Name      | Favorite Tater | GitHub                 | Twitter                                     | Title      |
|-----------|----------------|------------------------|---------------------------------------------|------------|
| Huth S0lo | Russian Blue   | [@huths0lo](@huths0lo) | [@Huth_S0lo](https://twitter.com/Huth_S0lo) | Moonshiner |