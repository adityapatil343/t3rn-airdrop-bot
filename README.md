Auto Bridge Bot
Auto Bridge Bot is a Python script to manage automated transactions between blockchain networks using Web3. This script supports networks like OP Sepolia, Base Sepolia, and others.

Feature
Auto Transactions : Send automatic transactions between selected networks.
Gas Estimate : Calculates the gas required for each transaction.
Balance Monitoring : Displays ETH and BRN balance after successful transaction.
Interaction with Explorer : Provides a direct link to the blockchain explorer for each transaction.
Interactive Menu : Select network and operating mode directly through the terminal.
Prerequisite
Before running the script, make sure you have installed and configured:

Python (Version 3.7 or later)
Python Dependencies :
web3
eth_account
Configuration File :
data_bridge.py: Contains data for each bridge.
keys_and_addresses.py: Contains the private key, address, and account label.
Installation
Clone this repository:

git clone https://github.com/adhe222/T3rn-bot.git
cd T3rn-bot
Install dependencies:

pip install web3 eth_account
File configuration:

Complete data_bridge.pywith bridge data.
Enter the private key and address into keys_and_addresses.py.
Usage
Run the script with the command:

python t3rn-bot.py
Select one of the options in the menu:

1 : OP -> Base Sepolia
2 : Base -> OP Sepolia
3 : Run all transactions repeatedly.
The script will process the transaction and display the results in the terminal, including:

Return address
Gases used
Block number
ETH and BRN balance
Link to blockchain explorer
keys_and_addresses.py
Example format:

private_keys = [
    "0xYourPrivateKey1",
    "0xYourPrivateKey2"
]

my_addresses = [
    "0xYourAddress1",
    "0xYourAddress2"
]

labels = [
    "Account 1",
    "Account 2"
]
data_bridge.py
Example of bridge data:

data_bridge = {
    "OP - BASE": "0xDataForOPToBaseBridge",
    "BASE - OP": "0xDataForBaseToOPBridge"
}
Security Notes
Never share your private key.
Make sure the configuration file is only accessed by you.
