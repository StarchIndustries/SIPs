---
SIP: 1
Title: Starch Improvement Proposals
Status: Pending
Category: Meta
Authors:
    - Abstract Potato <ipubliclife@gmail.com>
Implementors: N/A
Discussions:
    - None so far...
Created: 2024-01-09
License: CC-BY-4.0
---

## Abstract

A Starch Improvement Proposal (SIP) is a formalised design document for the Starch community and the name of the process by which such documents are produced and listed. A SIP  provides information or describes a change to the Starch ecosystem, processes, or environment concisely and in sufficient technical detail. In this SIP, we explain what a SIP is; how the SIP process functions; the role of the SIP Editors; and how users should go about proposing, discussing and structuring a SIP.

The Starch Foundation intends SIPs to be the primary mechanisms for proposing new features, collecting community input on an issue, and documenting design decisions that have gone into Starch. Plus, because SIPs are text files in a versioned repository, their revision history is the historical record of significant changes affecting Starch.

## Motivation: why is this SIP necessary?

SIPs aim to address two challenges mainly:

1. The need for various parties to agree on a common approach to ease the interoperability of tools or interfaces.

2. The need to propose and discuss changes to the protocol or established practice of the ecosystem.

The SIP process does not _by itself_ offer any form of governance. For example, it does not govern the process by which proposed changes to the Starch protocol are implemented and deployed. Yet, it is a crucial, community-driven component of the governance decision pipeline as it helps to collect thoughts and proposals in an organised fashion. Additionally, specific projects may choose to actively engage with the SIP process for some or all changes to their project.

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
      - [Naming SIPs with similar subjects](#naming-SIPs-with-similar-subjects)
    - [1.b. Authors seek feedback](#1b-authors-seek-feedback)
  - [2. Editors' role](#2-editors-role)
    - [2.a. Triage in bi-weekly meetings](#2a-triage-in-bi-weekly-meetings)
    - [2.b. Reviews](#2b-reviews)
  - [3. Merging SIPs in the repository](#3-merging-SIPs-in-the-repository)
  - [4. Implementors work towards Active status following their 'Implementation Plan'](#4-implementors-work-towards-active-status-following-their-implementation-plan)
- [Editors](#editors)
  - [Missions](#missions)
  - [Reviews](#reviews)
  - [Nomination](#nomination)

### Document

#### Structure

A SIP is, first and foremost, a document which proposes a solution to a well-defined problem. Documents are [Markdown][] files with a _Preamble_ and a set of pre-defined sections. SIPs authors must abide by the general structure, though they are free to organise each section as they see fit.
