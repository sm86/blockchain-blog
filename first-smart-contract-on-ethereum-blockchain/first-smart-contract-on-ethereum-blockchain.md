# Building Your First Smart Contract on Ethereum Blockchain

# Consensus on the expectations
*Blockchain*, fancy right? Smart contracts is fancy stuff in Blockchain itself which makes it lot more fancier. Smart contracts have crucial role in Blockchain ICOs, tokens and transactions too. They are programmable contracts which execute when the given conditions are met.

By the end of this tutorial, you will

* Write your Hello World smart contract in Solidity in the Remix IDE
* Deploy it on Ethereum test network using Metamask

# Before you Dive in!
As you have landed here, I am assuming you have basic knowledge of Blockchain technology, Ethereum and smart contracts. *If you have zero knowledge, No worries* [take a quick look at this article](https://medium.com/startup-grind/gentle-intro-to-blockchain-and-smart-contracts-part-1-3328afca62ab)
Make sure you have either Google Chrome or Mozilla Firefox or Brave Web Browsers

# The Background work
### MetaMask Setup
Metamask is a browser extension which allows users to run Ethereum dApp in the browser without running full Ethereum Node.
Lets first download Metamask.

* Firefox : https://addons.mozilla.org/en-US/firefox/addon/ether-metamask/
* Chrome : https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn

Now select MetaMask icon in your browser toolbar. After going through the *Privacy Notice*, **Accept** it.

![Accept the Privacy Notice](http://blocksofdata.com/wp-content/uploads/2017/12/MetaMaskPrivacyNotice.png)

Next, scroll down till the end to **Accept the Terms of Use**.

![Scroll and Accept the terms of use](http://blocksofdata.com/wp-content/uploads/2017/12/MetamaskTermsOfUse.png)

Now, *set the password* to sercure MetaMask wallet and tap on **Create** button.

![Set up password](http://blocksofdata.com/wp-content/uploads/2017/12/metamaskSetPassword.png)

Set up and store this seed phase safely, this helps to restore your accounts.

![Set up seed phase](http://blocksofdata.com/wp-content/uploads/2017/12/metamaskseed.png)

By default, we are in Ethereum Main network. Let us migrate to Rospsten Test Network for this tutorial purpose. To change the network, click on **Main Network** and change it to **Rospten Test Network** from the drop down.

![Select Ropsten Test Network](http://blocksofdata.com/wp-content/uploads/2017/12/metamaskRopsten.png)

Hmm... we have 0eth balance on this account. :( lets us hunt for some ether. Click on **Buy** button and select **Ropsten Test Facut** service. This opens up the below webpage, tap **request 1 ether from facut** to earn some balance in your account.

![Ropsten Facut MetaMask](http://blocksofdata.com/wp-content/uploads/2017/12/RopstenFaucetMetamask.png)
*Hurray, we have the MetaMask account with some ether now!* :D

### Remix IDE
Solidity is the language used for programming smart contracts in Ethereum. The Remix is an IDE for programming smart contracts in Solidity with an inbuilt compiler.
Open the Remix IDE: https://remix.ethereum.org

![Remix IDE Solidity](http://blocksofdata.com/wp-content/uploads/2017/12/RemixIDE.png)

# Diving into the Fun part
The battlefield is now set for us to start coding our smart contract.
If you are familiar with Object Oriented programming languages, Solidity would be so relatable.
Select **+** icon on top left corner of Remix IDE to create a new file and name it *HelloWorld.sol*
Let's dive into the code now. In the editor, add the below line.

    pragma solidity ^0.4.11;

pragma line is to specify the minimum compactable version of Solidity compiler.
You can correlate Contracts to classes in OOPs languages. To create our first contract, add the below code below pragma.

    contract HelloWorld{

    }

We will now define a variable in our contract declaration.

    string greeting;

We will define a constructor for our contract, below the variable declaration.

    function HelloWorld(string _greeting) public{
    greeting= _greeting;
    }

![Code](http://blocksofdata.com/wp-content/uploads/2017/12/CodeIDERemix.png)

On the top right, you can observe that the code is auto-compiled.

Yeah! We have successfully coded and compiled the contract. 8

# Let us go Live

In this section, we will see how to deploy the smart contract code onto Ethereum network.

Select the Run tab in the top right corner to open the below settings.

![Run Smart Contract](http://blocksofdata.com/wp-content/uploads/2017/12/RunIDE.png)

Make sure you have selected **Injected Web3** as the environment and the account has some ether in it.

Now type some string within double quotes as a parameter for our constructor. Just like **"Namaste"** in my contract below.

![Run Smart contract](http://blocksofdata.com/wp-content/uploads/2017/12/Namaste-Run-Smart-Contract.png)

And then press **Create** to deploy the contract onto the network.

![Confrm Smart Contract](http://blocksofdata.com/wp-content/uploads/2017/12/Confirm-smart-contract.png)

Select **Submit** in MetaMask dialogue box to deploy the contract.

![Contract Published](http://blocksofdata.com/wp-content/uploads/2017/12/Confirmation-Screen.png)

It might take few seconds for confirmation of your contract. You will get a confirmation message in your console with block no and transaction ID.

MetaMask maintains all your interactions with the network. By clicking on the recent contract in MetaMask, we are redirected to EtherScan.

Etherscan is an Ethereum Blockchain explorer, we can use this portal to verify our transaction as below.

![Ether Scan](http://blocksofdata.com/wp-content/uploads/2017/12/Etherscan.png)

Hurray! You are now a master in the smart contract development on Ethereum network. ;)

## What's next
Go through the [Solidity Documentation](https://solidity.readthedocs.io/en/develop/)

Truffle framework for DApps Development. Stay tuned! I will write my blog on the same by second week of Jan.

> Thanks for reading. In case you are stuck /have any queries or want to share your views please comment below or mail me at shashank.motepalli@gmail.com