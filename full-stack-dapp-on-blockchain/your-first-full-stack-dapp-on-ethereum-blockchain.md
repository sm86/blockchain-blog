# Your first Full Stack DApp on Ethereum Blockchain
# Consensus on the expectations

DApps(Decentralized Applications) are built as over the top services on the blockchain network.

This tutorial is designed to give you a head-start to DApp development on Ethereum Blockchain. Through this tutorial, we will accomplish the following:

* Setup the DApp development environment
* Setup local blockchain network with Ganache-cli (previously *testrpc*)
* Compile and deploy the contracts into network
* Interact with DApp in your browser

# Before you dive in

A basic knowledge of Ethereum, HTML and JavaScript would be ideal. I would suggest you have a look at the tutorial on [your first smart contract on Ethereum blockchain](http://blocksofdata.com/first-smart-contract-on-ethereum-blockchain/). *Make sure you followed **MetaMask setup** from above tutorial and have it installed on your browser.*

# The Background Work

[*Truffle*](http://truffleframework.com/) is development environment and asset pipeline for Ethereum development. Truffle makes our life of a smart contract developer much simpler.

First of all, verify installation of Node.js v6+. If not, you can install from their official site. [Download Node.js](https://nodejs.org/en/download/)

![truffle install](http://blocksofdata.com/wp-content/uploads/2018/01/NodeJs-and-truffle-verify.png)

Let us now install truffle framework and confirm the same.
> npm install -g truffle

# Setting up the project structure

Create a folder Metacoin for purpose of this tutorial and navigate into it.
> mkdir metacoin
cd metacoin

Truffle can be used to initialize the current directory with base project structure.
> truffle unbox webpack

![truffle unbox](http://blocksofdata.com/wp-content/uploads/2018/01/Truffle-unbox-and-ls.png)

As you can see, truffle creates all necessary files and folders to run a full stack DApp. You will have the following project structure:

* **contracts/** : Contains Smart contracts written in Solidity. To learn more, refer [Solidity Contracts](http://truffleframework.com/docs/getting_started/contracts)
* **migrations/** : Contains migrations files which are used for deploying contracts onto blockchain. To learn more, refer [Running Migrations](http://truffleframework.com/docs/getting_started/migrations)
* **truffle.js** : Truffle configuration file
* **app/** : Contains HTML/JavaScript files of the dapp.

# Setting up our local Blockchain network

For this tutorial, we will restrict ourselves to Ganache CLI (previously *testrpc*), a personal blockchain for Ethereum development. Think of this as blockchain simulation environment.
Let us first install Ganache CLI. Open up a *new terminal and navigate to metacoin* folder and install.
> npm install -g ganache-cli

![testrpc install](http://blocksofdata.com/wp-content/uploads/2018/01/Install-testrpc-ganache.png)

After its installation, let us start the environment by typing **ganache-cli** in the command line.

![Ganache CLI network](http://blocksofdata.com/wp-content/uploads/2018/01/Ganache-CLI.png)

*Boom!* The local blockchain is now running on port 8545 and it has created 10 accounts for us with 100 ether in each.

As we are going to have a DApp on the browser, we want MetaMask to get synced with this local network. First, copy the **mnemonic** from the console.
Now, open MetaMask in your browser and select **Restore from Seed Phase**. In case, you are already logged in, select **Lock** from setting to see the below screen.
![Restore from seed phase](http://blocksofdata.com/wp-content/uploads/2018/01/Restore-from-Seed-Phase.png)

The time has arrived to paste your copied mnemonic. Choose your password and confirm it.

![Metamask Ganache](http://blocksofdata.com/wp-content/uploads/2018/01/Metamask-Ganache-.png)

Change the network to *Local Host 8545*.

![Local host 8545 Metamask](http://blocksofdata.com/wp-content/uploads/2018/01/Localhost-8545-network.png)

*Hurray, we are now on our local blockchain network!* Do not close this terminal, keep the network running.

# Time to compile and deploy
To compile our smart contracts present in *contracts/* folder
> truffle compile

![truffle compile](http://blocksofdata.com/wp-content/uploads/2018/01/compile-truffle.png)

Since our local blockchain is on port 8545. Let us now change **port** in the truffle.js configuration file from 7545 to **8545**.

![Port number to 8545](http://blocksofdata.com/wp-content/uploads/2018/01/Port-number-truffleJS-.png)

We will now deploy the contract onto the blockchain.
> truffle migrate

![truffle migrate](http://blocksofdata.com/wp-content/uploads/2018/01/truffle-migrate.png)

*Yipee, we have our contract deployed onto the network.* You can verify the same by observing ganache-cli console.

# Running our DApp on browser
So what's next? A user interface may make our application complete. Truffle webpack has set basic structure for us in *app/* folder. Let us start the server
> npm run dev

![Start the server](http://blocksofdata.com/wp-content/uploads/2018/01/start-Server.png)

Open up [http://localhost:8080](http://localhost:8080) in your browser to see the below page.

![Metacoin home screen](http://blocksofdata.com/wp-content/uploads/2018/01/Metacoin-Fill-in-values.png)

The webpage shows that we have 10000 metacoin balance. Enter some arbitrary values in Amount and address, say *100 and 0x123456789123456789123456789*. Now select the option to **Send Metacoin**

![Confirm the payment](http://blocksofdata.com/wp-content/uploads/2018/01/MetaMask-Confirmation-Metacoin.png)

A MetaMask window pops up for your approval. accept the transaction. Select **Submit**

![Confirmation message](http://blocksofdata.com/wp-content/uploads/2018/01/Page-Updated-after-transaction-1.png)

On refreshing the page, you can see that your balance is updated. The transaction also appears in MetaMask transaction history.
The transaction can be verified in your ganache-cli console as below.

![Console conformation](http://blocksofdata.com/wp-content/uploads/2018/01/Console-Ganachi-cli-conformation.png)

**Congratulations my friend, you are all set to be a full stack DApp developer.** :D In this tutorial, we have set up the environment, used truffle to compile and deploy the contract. We also ran the web app to interact with our contract.
# What's next?
* Now that you got a feel for DApp development, you can try building a basic application for your use case.
* Configure your DApp for live test network of Ethereum

> Thanks for reading. In case you are stuck /have any queries or want to share your views please comment below or mail me at shashank.motepalli@gmail.com
