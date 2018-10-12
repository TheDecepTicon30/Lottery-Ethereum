# Lottery-Ethereum
An Ethereum based solidity smart contract written for randomly picking up lottery winners.

# Smart Contract
The lottery.sol is written in solidity v0.4.17 which contains the smart contract written for randomly picking up lottery winners. You can also add participants to the contract by donating 0.01 ether to the manager. The manager will be the one who deploys the smart contract. Only the manager can run the pickWinner() function which finds out the winner of the lottery. We have calculated random number by using keccak256 algorithm which calculates a random number in 256 bytes. This number is then typecasted to uint. We also add a require statement in pickWinner() which checks if the function is called by the manager or not. If not, then this function will not return anything. 
You can read more about smart contracts [here.](https://en.wikipedia.org/wiki/Smart_contract)
You can read more about the solidity language [here.](https://solidity.readthedocs.io/en/v0.4.25/)
You can read more about the keccak256 algorithm [here.](https://solidity.readthedocs.io/en/v0.4.21/units-and-global-variables.html)

# Compiling the Smart Contract
To compile the smart contract we will be using solc compiler which is used to compile solidity codes. The compile code is placed in compile.js. 
The code is written in [JavaScript.](https://en.wikipedia.org/wiki/JavaScript)

# Testing our Smart Contract
The lottery.test.js file, written in JavaScript tests our smart contracts by using multiple testcases written in it. We will be using mocha as the testing framework. 
Read more about mocha [here.](https://mochajs.org/) 

# Deploying our Smart Contract
The deploy.js file will deploy our smart contract to the Rinkeby Test Network. This network is similar to the main Ethereum Network but the only difference is that we don't need to pay for deploying our smart contracts. It works completely on the concept of virtual money.

# Steps to configure the project and to run our Smart Contract and deploy it on Rinkeby TestNet.
1) Create a folder named Lottery in your working directory.
2) Create a folder named contracts in Lottery and sace our smart contract in this folder.
3) Place the compile.js and deploy.js in the folder Lottery itself.
4) Create a folder named test and save the lottery.test.js here.
5) Install NodeJS in your computer from [here.](https://nodejs.org/en/) Use the recommended version.
6) Install Git in your computer from [here.](https://git-scm.com/downloads)
7) Open up your cmd. Navigate to the folder Lottery in your cmd. 
8) Run the command- 'npm init' in our Lottery folder. This will create a package.json file in your directory.
9) Install packages Truffle, Mocha, Ganache-CLI and Web3 by running the command 'npm install --save truffle-hdwallet-provider@0.0.3    mocha ganache-cli web3'. Truffle is a development environment, testing framework and asset pipeline for Ethereum. Mocha is a testing framework which will be required by our lottery.test.js file. Ganache provides a environment for truffle. Web3 is a collection of libraries which allows you to interact with a local or remote ethereum node.
10) To compile our smart contract, run command 'node compile.js'. 
11) To test our smart contract, run 'npm run test'.
12) Install MetaMask which is an extension for browsers like Chrome to easily track your transactions and accounts.
13) Finally, deploy our contract on the Rinkeby network by running command 'node deploy.js'
