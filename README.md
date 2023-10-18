# Blockchain: PyChain Ledger
The aim of this project is to build a blockchain-based ledger system for banks to conduct financial transactions with a simple to use web interface.

## The Chain

The chain of blocks records a ledger of history consisted with 3 information:
* Sender Name
* Receiver Name
* Amount

As a basic block chain, each block of the ledger history also includes features:
* Creator ID
* Previous Hash
* Nonce
* Timestamp

We use SHA256 to calculate the hash of all information.

## About
Decentralized finance is the new way to conduct financial transactions without the need for a itermediary body such as a bank. By using a blockchain-based ledger system, financial transactions can be conducted with the ability for the data to be verified at anytime in the ledger. This includes the sender, receiver, amount and time of the transactions. Due to the nature of the blockchain any transactions that has been hashed to a block cannot by changed or overwritten. This ensures the integrity of all the data stored in the ledger.

## Getting Started
To run the Jupyter notebook and interact with the visualizations, you need to have the following software and Python libraries installed:

- Python 3.10 or later
- Streamlit

## Installing
1. Install the latest verion of Python [here](https://www.python.org/downloads/).

2. To install the Streamlit packages, run the following command in your terminal.

```
pip install Streamlit
```

## Usage
You can clone or download this GitHub project and open the `pychain.py` using any IDE of your choice, one being Visual Studio Code. In the terminal, navigate to the folder that the `pychain.py` file is located. Run the streamlit application by running the following command. 

```
streamlit run pychain.py
```

Values for the sender, receiver and amount can be entered before clicking "Add Block" to add the transaction to the ledger.

The blockchain and transactions can then later be verified by clicking the "Validate Chain" button.

# Report
## Testing the Web Application
## The Tests

As one of the aspects to explore, levaraging streamlit, the targeting hash is alllowed to have leading zeros from 1 to 6, according to which the Nonce is mined, called "proof of work".

Only with the proper nonce meeting the target leading zero, a new block can be added to the chain.

When the difficulty of mining the nonce is high, we can pause the mining instead of running and waiting forever.

One other test is to check if the chain is a valid one, i.e., each block having its previous hash stored authenticated. If any block in the chain is changed, this validation will fail.

We also provide a function to try and change some information then validate the chain. Interestingly, we found that the last block can be changed without issue, but previous blocks cannot.

## Demo

### Build the chain

From a preset "genesis" block, we can input the information to build a new block, then add it to the chain.
![Add a block](Images/add_block.png)

### See the chain

Whenever a new block is added, the "chain view" extends to show it.
![The chain](Images/the_chain.png)

### Validate chain

Click the Validate Chain button, if the chain is validated, the ledger is displayed for easy read.

### Pause during long-run mining

High difficulty

![6 zeros](Images/high_difficulty_with_block_inspector.png)

Toggle to pause mining

![pause](Images/pause_mining.png)

### Valid change

We can change the last block
![last block change](Images/change_last_block.png)

### Invalid change

Change the first block (it does not have ledger info!)
![1st block change](Images/change_1st_block.png)

It's invalid!

![invalid](Images/invalid_change.png)

### Continuing End

* If we change back the info, the chain becomes valid again.
* We have a Rerun button which if you click the chain starts from afresh

## Contributor
Harshita Panchal
