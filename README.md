# 🧱🔗 Proof_of_Authority_Development_Chain 🧱🔗
Setting up a custom testnet blockchain, send a transaction, create a repository, and document the steps of how this process is done.
This tutorial will provide you with step-by-step instructions on how to create your own private Proof of Authority Blockchain.

## What you need to get started
* [Geth](https://geth.ethereum.org/docs/install-and-build/installing-geth)
This is the toolset used to create your nodes and blockchain
* [MyCrypto](https://download.mycrypto.com/)
This is the application we will use to maintain your Ethereum accounts and conduct a trade from one account to another

## Create Nodes
Unzip the Geth CLI toolset and open a git bash terminal from the unzipped folder(I renamed my folder "gethPoA")
![](Screenshots/1unzip_geth_alltools_folder.png)
![](Screenshots/2open_terminal_in_unqipped_folder.png)

In git bash, run the following code to create your first node(node1). You will need to create a password, and SAVE THAT PASSWORD!
geth --datadir node1 account new
Your node will have a public address key and a secret key file automatically generated. SAVE THESE! I have listed mine below, but you should always keep your secret key file private. DO NOT SHARE WITH ANYONE OR ONLINE!
Public address of the key:   0x4636FA8cd9b0287d1031312F36FBfc0f7773396b
Path of the secret key file: node1\keystore\UTC--2021-08-27T03-27-56.842659500Z--4636fa8cd9b0287d1031312f36fbfc0f7773396b
![](Screenshots/3create_node1.png)

Repeate this same process for your second node(node2). Save the password that you generate, as well as the public address and secret file
geth --datadir node2 account new
Once again, I have shared mine, but you should NEVER SHARE WITH ANYONE OR ONLINE!
Public address of the key:   0x6007BEe74Bc3896079314B93bfa2Ee22f5509741
Path of the secret key file: node2\keystore\UTC--2021-08-27T03-31-01.280518400Z--6007bee74bc3896079314b93bfa2ee22f5509741
![](Screenshots/4create_node2.png)

You will notice that new folders have been populated into your unzipped folder labeled as what you named your nodes(node1 & node2)
![](Screenshots/5_new_folders_populated_nodes.png)

## Create Proof of Authority network and Genesis Block
In your terminal(git bash) from your unzipped folder, we are going to create our Proof of Authority network. First, run this code to open your Ethereum private network manager.
./puppeth
* Specify a network name(poa1)
* Configure new genesis(option 2)
* Create a new genesis from scratch(option 1)
* Specificy that we want a proof-of-authority consensus engine(option 2)
* Use default 15 second blocks
* List which accounts are allowed to be sealed. Use the public address keys for node1 and node2
* List the public address keys for node1 and node2 as accounts that should be pre-funded
* Answer "no" when asked if the precompiled-addresses should be pre-funded with 1 wei
* Lastly, specify your chain/network ID. Do not generate a random chainID, but rather pick a number(777) and SAVE THAT CHAINID NUMBER!
![](Screenshots/6configure_poa.png)

* Now that we've got our PoA network and genesis block created, let's manage existing genesis(option 2).
* Export genesis configurations(option 2).
* Press enter create the JSON files.
![](Screenshots/7create_genesis_block.png)

You will notice that 2 new JSON files have been added to your unzipped gethPoA folder, poa1.JSON and poa1-harmony.JSON
![](Screenshots/8poa1_poa1harmony_JSON.png)

If you open the poa1.JSON file, you will see the genesis block. This is where you can find your chainID if you forgot to write it down, as well as other info on the genesis(first) block in your network.
![](Screenshots/9genesis_block.png)

