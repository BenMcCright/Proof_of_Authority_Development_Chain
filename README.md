# 🧱🔗 Proof_of_Authority_Development_Chain 🧱🔗
Setting up a custom testnet blockchain, send a transaction, create a repository, and document the steps of how this process is done.

This tutorial will provide you with step-by-step instructions on how to create your own private Proof of Authority Blockchain.
## What you need to get started
* [Geth](https://geth.ethereum.org/docs/install-and-build/installing-geth)
This is the toolset used to create your nodes and blockchain
* [MyCrypto](https://download.mycrypto.com/)
This is the application we will use to maintain your Ethereum accounts and conduct a trade from one account to another

## Create Nodes
Unzip the Geth CLI toolset and open a git bash terminal from the unzipped folder
![](Screenshots/1unzip_geth_alltools_folder.png)
![](Screenshots/2open_terminal_in_unqipped_folder.png)

In git bash, run the following code to create your first node(node1). You will need to create a password, and SAVE THAT PASSWORD!
geth --datadir node1 account new
Your node will have a public address key and a secret key file automatically generated. SAVE THESE!
![](Screenshots/3create_node1.png)

Repeate this same process for your second node(node2). Save the password that you generate, as well as the public address and secret file.
geth --datadir node2 account new
![](Screenshots/4create_node2.png)

You will notice that new folders have been populated into your unzipped folder labeled as what you named your nodes(node1 & node2).
![](Screenshots/5_new_folders_populated_nodes.png)