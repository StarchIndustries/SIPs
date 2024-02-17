# Inverse Potato Rewards Curve
`SIP: 69420`
`Status: Pending`
`Category: StarchPools`
#### Authors: Abstract Potato <ipubliclife@gmail.com> / Bone Pool
## Problem:
There aren't enough incentives for delegators to chose to stake to smaller pools within the list of Starch Pools.

## Proposed Solution:
A system that can **push delegation to the edges** by providing higher reward percentages to smaller stake pools.

#### Implementation:
1. Get all Stake Pools and their active stake.
2. Determine total amount of delegation among all pools.
3. Determine Percentages of the total held by each pool.
4. Sort from smallest to largest pool.
5. Reverse the list and use percentage to determine rewards.
6. If any pool has a percentage below 6.9420% set their rank to this amount.

## Citations:
None
