---
CIP: 1
Title: Cardano Improvement Proposals
Status: Active
Category: Meta
Authors:
    - Frederic Johnson <frederic@advanceweb3.com>
    - Sebastien Guillemot <sebastien@dcspark.io>
    - Matthias Benkort <matthias.benkort@cardanofoundation.org>
    - Duncan Coutts <duncan.coutts@iohk.io>
    - Michael Peyton Jones <michael.peyton-jones@iohk.io>
Implementors: N/A
Discussions:
    - https://github.com/cardano-foundation/cips/pull/366
    - https://github.com/cardano-foundation/cips/pull/331
    - https://github.com/cardano-foundation/CIPs/tree/3da306f3bfe89fa7de8fe1bf7a436682aeee25c5/CIP-0001#abstract
Created: 2020-03-21
License: CC-BY-4.0
---

## Abstract

A Cardano Improvement Proposal (CIP) is a formalised design document for the Cardano community and the name of the process by which such documents are produced and listed. A CIP  provides information or describes a change to the Cardano ecosystem, processes, or environment concisely and in sufficient technical detail. In this CIP, we explain what a CIP is; how the CIP process functions; the role of the CIP Editors; and how users should go about proposing, discussing and structuring a CIP.

The Cardano Foundation intends CIPs to be the primary mechanisms for proposing new features, collecting community input on an issue, and documenting design decisions that have gone into Cardano. Plus, because CIPs are text files in a versioned repository, their revision history is the historical record of significant changes affecting Cardano.

## Motivation: why is this CIP necessary?

CIPs aim to address two challenges mainly:

1. The need for various parties to agree on a common approach to ease the interoperability of tools or interfaces.

2. The need to propose and discuss changes to the protocol or established practice of the ecosystem.

The CIP process does not _by itself_ offer any form of governance. For example, it does not govern the process by which proposed changes to the Cardano protocol are implemented and deployed. Yet, it is a crucial, community-driven component of the governance decision pipeline as it helps to collect thoughts and proposals in an organised fashion. Additionally, specific projects may choose to actively engage with the CIP process for some or all changes to their project.

## Specification

### Table of Contents

- [Document](#document)
  - [Structure](#structure)
    - [Header Preamble](#header-preamble)
    - [Translations](#translations)
    - [Repository Organization](#repository-organization)
    - [Licensing](#licensing)
  - [Statuses](#statuses)
    - [Status: Proposed](#status-proposed)
    - [Status: Active](#status-active)
    - [Status: Inactive](#status-inactive)
  - [Path to Active](#path-to-active)
  - [Categories](#categories)
  - [Project Enlisting](#project-enlisting)
- [Process](#process)
  - [1. Early Stage](#1-early-stages)
    - [1.a. Authors open a pull request](#1a-authors-open-a-pull-request)
      - [Naming CIPs with similar subjects](#naming-cips-with-similar-subjects)
    - [1.b. Authors seek feedback](#1b-authors-seek-feedback)
  - [2. Editors' role](#2-editors-role)
    - [2.a. Triage in bi-weekly meetings](#2a-triage-in-bi-weekly-meetings)
    - [2.b. Reviews](#2b-reviews)
  - [3. Merging CIPs in the repository](#3-merging-cips-in-the-repository)
  - [4. Implementors work towards Active status following their 'Implementation Plan'](#4-implementors-work-towards-active-status-following-their-implementation-plan)
- [Editors](#editors)
  - [Missions](#missions)
  - [Reviews](#reviews)
  - [Nomination](#nomination)

### Document

#### Structure

A CIP is, first and foremost, a document which proposes a solution to a well-defined problem. Documents are [Markdown][] files with a _Preamble_ and a set of pre-defined sections. CIPs authors must abide by the general structure, though they are free to organise each section as they see fit.
