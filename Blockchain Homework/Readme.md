# ZBank Blockchain Homework
#### This homework represents the creation of my own miniature blockchain, along with a test transaction,using Ethereum. In the creation of this blockshain, I initially used the proof of authority consensus algorithm to set up the network. However, too many facets within the final node setup kept the nodes from mining and communicating with each other. For this reason, the test transaction was sent using a network built with the proof of work consensus.

##  Setup
1. ### Create accounts for nodes 1 and 2
    #### Within Git Bash, we navigate to the file that contains our blockchain tools. We use geth to create two new accounts that we will use for nodes 1 and 2. We us the passwords 'homework1' and 'homework2' respectively. We make sure to save both the public key and the path of the secret key file to a cheat sheet. If this were a real Ethereum network with money involved, we would be sure to either write these down or save them to a removable thumb drive.


2. ### Set up the network
    #### Using puppeth, we create a brand new network for the ZBank testnet. Our goal is to create this blockchain from scratch, so we select #2 and #1 in order to create a brand new genesis block. We choose proof-of-work and designate which accounts we want to be pre-funded. Using the proof of authority, we would also have to choose which accounts can seal the blocks. We then set our Chain ID to 829.

    #### Next, we navigate to "Manage existing genesis" in order to export the configurations for the genesis block. This generates four json files, and for the purposes of beginning to mine, we are interested in the zbank_testnet.json file

3. ### Execution
    #### To execute the genesis block and begin mining, we first initiate both nodes using the .json file we created above. After initiating both nodes we are ready to begin mining.
    #### We start the first node as the mining node, making sure that the account is unlocked and using one minerthread. We execute the mining command and immediately search in the response for the enode so that we can start the second node.
    #### Using the enode we copied from the response of the first node, we start the second node so that it tracks all blocks that are mined and sealed imports each chain segment.

4. ### Using This Blockchain to Send Transactions
    #### In order to send transactions through this blockchain network, the user can open the MyCrypto app and, within the zbank_testnet4 network, unlock their wallet. 
    #### We created a new node using the network name chain ID in order to create this network, and then we used our private key to open our wallet within that network. This network uses Ethereum as its currency, so the user can input the address they are sending to, the amount they would like to send, increase or decrease the transaction fee, and send the transaction. The transaction appears in the blockchain on the ledger and the transaction is tracked as a success.