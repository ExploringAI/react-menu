## What it does
- a distributed large file repository similar to Github but with no file size restriction	
	- Files would be shared across the network using IPFS
	- The network would need to be defined as a number of clusters 
	- Each file would be split into a number of blocks and assigned to a cluster
		- Additionally, each block would be checksummed with something like MD5 for security
		- Blocks are replicated across a cluster for redundancy in case a node goes down within
		a cluster
		- Blocks should be versioned to allow for file updates (see Github's DAG schema for
		an example of versioning)
	- The only thing stored globally on-chain is the metadata of the file such as its name, UUID,
	block information and the clusters responsible for it
	- Essentially operating two blockchains:
		- A global ledger for file block metadata (primary chain)
		- A cluster local ledger for actual file blocks (secondary chain)
	- Would require a well-defined protocol for chain-to-chain communication
		- This should be able to be provided by a Kasuma feature (or set of features)
	- Would also require the development of an economic model to incentivize clients yielding
	storage space for the secondary chain
	- This particular idea is pretty much the BitTorrent protocol but for Blockchains
		- Unlike BitTorrent, by using a Blockchain, security improves as we can guarantee files
		have not been tampered with
	- May require the implementation of a custom consensus mechanism

General Architecture: https://drive.google.com/file/d/160s45LosRJXrg80aMVbO1FWnfrFssf87/view?usp=sharing


In order for the router to work, must download react-router-dom:

$ npm install --save react-router-dom
(Note, you may not have to do this if it is already pre-installed)

$ npm install bootstrap
