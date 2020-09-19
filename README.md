# hadcoin
Following the tutorial, created a Custom Cryptocurrency

Using Flask to Deploy this application.

Objective:

To build a cryptocurrency using a blockchain and simulate the events of mining and solving the cryptographic puzzle.


Function Descriptions:

1. init: Initializing the genesis block

2. create_block: Takes the previous hash and the proof to add to 
the blockchain.

3. get_previous_block: Returns the previous block in the chain

4. proof_of_work: Taking a constant difficulty here, the algorithm used here is a random one. Using SHA256 to check the first 4 characters. Keep iterating until found.

5. hash: Returns SHA256 of the block.

6. is_chain_valid: Iterating over each block in the chain. Checking if the previous_hash in each block is actually the previous one. Check if the proof is valid

7. add_transaction: Find the previous block and add the transaction to the next index

8. add_node: Adding node to the netwok 

9. replace_chain: The longest chain needs to be cascaded throughout the network. Iterating over each of the nodes and fetching the largest chain, and updating it.

Flask Endpoints:
	
	1. mine_block: Mining the block by following the steps. First add the transaction, then create the block
	
	2. get_chain: Return the blockchain and the length

	3. is_valid: Returns the status of the Blockchain whether it is valid.
	
	4. add_transaction: Given a JSON input containing sender receiver and amount we get the transaction added. In transaction.json a sample is shown.

	5. connect_node: Used to create the network. Shown in nodes.json. For each node the rest must be used in the json. i.e Remove the current node.

	6. replace_chain: Update the chain to reflect the longest one.
