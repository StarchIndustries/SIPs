# Block creation with VRF (Verifiable Random Function)
`SIP: 2`
`Status: Pending`
`Category: Meta`
#### Authors: Abstract Potato <ipubliclife@gmail.com> / Adam K Dean
## Problems:
- Currently there isn't a way to verify how blocks are being selected from the `pending_blocks` list.
## Proposed Solution
### Create a system that uses either internal Starch-Chain data to maintain a seperate system from cardano.
#### Implementation:
```python
last_block =  blockchain.get_last_block()
hash = last_block["hash"]
miners_str = '-'.join(miner_ids) # list of miners who submitted a block
block_id = last_block["id"]
random.seed = crypto.sha256(f'{hash}{miners_str}{block_id}')
winner = random.choice(pending_blocks)
```
### Fully integrate Cardano's VRF system by utilizing elements existing in Cardano.
#### Implementation:
```python
random.seed = cardano.latest_block()["hash"]
winner = random.choice(pending_blocks)
```
## Additional Resources:
- Python's Random function: https://docs.python.org/3/library/random.html
