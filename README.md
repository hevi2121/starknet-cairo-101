# Starknet Cairo 101 Automated Workshop

![banner](assets/banner.png)

Hey there! 

This tutorial is perfect for developers who are interested in learning how to read Cairo code and Starknet smart contracts. With this simple tutorial, you'll be able to get started in no time. Have fun!

## Introduction​

Welcome to Starknet, a general-purpose Validity Rollup on the Ethereum mainnet. It's a layer 2 scaling solution that lets developers build applications on top of Ethereum without compromising security, decentralization, and censorship resistance.

This workshop is designed to help you read Cairo code and Starknet smart contracts to understand syntax. Don't worry, you don't need to code or install anything on your machine to follow and complete it. **You can do it all from your browser**.

The workshop is a set of smart contracts deployed on Starknet Alpha on testnet. Each smart contract is an exercise/puzzle that outlines a feature of the Cairo Smart contract language.

Completing the exercises will earn you points in the form of an [ERC20 token](contracts/token/TDERC20.cairo). The token may not have any monetary value, but it's a fun way to get you to complete the exercises.

Hope you have fun participating in this workshop!

## What you will learn

- How to read Cairo code
- How to read Starknet smart contracts
- How to interact with Starknet smart contracts using Argent X, Braavos, and a Block Explorer.

### Disclaimer

​Don’t expect any benefit from using this other than learning some cool stuff about Starknet, the first general-purpose Validity Rollup on the Ethereum mainnnet.

​Starknet is still in Alpha. This means that development is ongoing, and the paint is not dry everywhere. Things will get better, and in the meanwhile, we make things work with a bit of duct tape here and there!​

## Steps

![Steps](assets/steps.png)

### 1. Creating a smart contract wallet and connecting it to a Block Explorer

**To complete the tutorial, you need to collect points.** You will own these points through your Starknet wallet. However, thanks to Account Abstraction, Starknet wallets work differently than Ethereum wallets. Do not worry; we will walk you through creating a wallet and connecting it to a Block Explorer.

- The easiest way to set one up is to use Argent X ([download the chrome extension](https://chrome.google.com/webstore/detail/argent-x-starknet-wallet/dlcobpjiigpikoobohmabehhmhfoodbb/)  or  [check their repo](https://github.com/argentlabs/argent-x)) or Braavos ([download the chrome extension](https://chrome.google.com/webstore/detail/braavos-wallet/jnlgamecbpmbajjfhmmmlhejkemejdma)). 
These wallet solutions are similar to what Metamask is for Ethereum and allow users to initiate transactions and interact with applications on Starknet.
- Follow the instructions in your wallet app to install the extension. It may take approximately 5 minutes for the account to be deployed. Note that in Starknet, there is only one type of account: smart contract accounts. This is called Account Abstraction, which is in contrast to Ethereum where there are wallets and smart contracts. In Starknet, every wallet is a smart contract, and there is no distinction between them and other smart contracts. To create a new wallet, you need to deploy a transaction that publishes your smart contract wallet to the network.
- Make sure you are on the Goerli testnet network.
- The tutorial’s points are held in contract  `WIP` ([Starkscan link](WIP), [Voyager link](WIP)). Click "Add Token" in your installed wallet and add the tutorial contract address so that your points balance appears there. A new token called `SC101` (starknet-cairo-101) will appear in your wallet.
- To execute transactions on the Goerli Starknet testnet, you will need testnet ETH to pay for gas. To obtain testnet ETH, go to the [faucet](https://faucet.goerli.starknet.io/) and follow the instructions. It may take several minutes, but you should receive some L2 Goerli ETH in your wallet that you can use to execute transactions on the testnet.

### 2. Use a Block Explorer to interact with the contracts

In this workshop we need to interact with a Block Explorer to solve the exercises.

Connect the Block Explorer ([Starkscan](https://testnet.starkscan.co/) or [Voyager](https://goerli.voyager.online/)) to your smart account contract (your Argent or Braavos wallet). These are Block Explorers for Starknet (the equivalent of Etherscan for Ethereum) and allow you to browse the state of the blockchain and view all transactions and their status. By connecting a Block Explorer to your wallet, you will be able to broadcast your transactions through your wallet and interact with the contracts in the tutorial.

When looking for a contract/transaction, always ensure you are on the Goerli version of the Block Explorer. To solve the exercises, access the contract’s `read`/`write` functions in the “read/write contract” tab in the Block Explorer.​

### 3. Solving exercises and getting points​
​
**Each exercise is a separate smart contract.** It contains code that, when executed correctly, will distribute points to your address.

Follow the instructions in each exercise in the `src` folder to get the points. Points are distributed by the function `distribute_points()` while `validate_exercise` records that you completed the exercise (you can get points only once).

Each exercise is deployed on the Goerli testnet, and you will need to interact with them through a Block Explorer. You can find the addresses of the contracts in the table below. In other words, if you want to interact with the exercise `Ex01`, you must open the contract address `WIP` in the Block Explorer.

| Topic                                 | Contract code                                         | Contract on Starkscan                                                                                              | Contract on Voyager                                                                                              |
| ------------------------------------- | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Points counter ERC20                  | [Points counter ERC20](contracts/token/TDERC20.cairo) | [Link](https://testnet.starkscan.co/contract/0x5c6b1379f1d4c8a4f5db781a706b63a885f3f9570f7863629e99e2342ac344c) | [Link](https://goerli.voyager.online/contract/0x5c6b1379f1d4c8a4f5db781a706b63a885f3f9570f7863629e99e2342ac344c) |
| General syntax                        | [Ex01](contracts/ex01.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x29e2801df18d7333da856467c79aa3eb305724db57f386e3456f85d66cbd58b) | [Link](https://goerli.voyager.online/contract/0x29e2801df18d7333da856467c79aa3eb305724db57f386e3456f85d66cbd58b) |
| Storage variables, getters, asserts   | [Ex02](contracts/ex02.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x18ef3fa8b5938a0059fa35ee6a04e314281a3e64724fe094c80e3720931f83f) | [Link](https://goerli.voyager.online/contract/0x18ef3fa8b5938a0059fa35ee6a04e314281a3e64724fe094c80e3720931f83f) |
| Reading and writing storage variables | [Ex03](contracts/ex03.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x79275e734d50d7122ef37bb939220a44d0b1ad5d8e92be9cdb043d85ec85e24) | [Link](https://goerli.voyager.online/contract/0x79275e734d50d7122ef37bb939220a44d0b1ad5d8e92be9cdb043d85ec85e24) |
| Mappings                              | [Ex04](contracts/ex04.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x2cca27cae57e70721d0869327cee5cb58098af4c74c7d046ce69485cd061df1) | [Link](https://goerli.voyager.online/contract/0x2cca27cae57e70721d0869327cee5cb58098af4c74c7d046ce69485cd061df1) |
| Variable visibility                   | [Ex05](contracts/ex05.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x399a3fdd57cad7ed2193bdbb00d84553cd449abbdfb62ccd4119eae96f827ad) | [Link](https://goerli.voyager.online/contract/0x399a3fdd57cad7ed2193bdbb00d84553cd449abbdfb62ccd4119eae96f827ad) |
| Functions visibility                  | [Ex06](contracts/ex06.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x718ece7af4fb1d9c82f78b7a356910d8c2a8d47d4ac357db27e2c34c2424582) | [Link](https://goerli.voyager.online/contract/0x718ece7af4fb1d9c82f78b7a356910d8c2a8d47d4ac357db27e2c34c2424582) |
| Comparing values                      | [Ex07](contracts/ex07.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x3a1ad1cde69c9e7b87d70d2ea910522640063ccfb4875c3e33665f6f41d354a) | [Link](https://goerli.voyager.online/contract/0x3a1ad1cde69c9e7b87d70d2ea910522640063ccfb4875c3e33665f6f41d354a) |
| Recursions level 1                    | [Ex08](contracts/ex08.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x15fa754c386aed6f0472674559b75358cde49db8b2aba8da31697c62001146c) | [Link](https://goerli.voyager.online/contract/0x15fa754c386aed6f0472674559b75358cde49db8b2aba8da31697c62001146c) |
| Recursions level 2                    | [Ex09](contracts/ex09.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x2b9fcc1cfcb1ddf4663c8e7ac48fc87f84c91a8c2b99414c646900bf7ef5549) | [Link](https://goerli.voyager.online/contract/0x2b9fcc1cfcb1ddf4663c8e7ac48fc87f84c91a8c2b99414c646900bf7ef5549) |
| Composability                         | [Ex10](contracts/ex10.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x8415762f4b0b0f44e42ac1d103ac93c3ea94450a15bb65b99bbcc816a9388)   | [Link](https://goerli.voyager.online/contract/0x8415762f4b0b0f44e42ac1d103ac93c3ea94450a15bb65b99bbcc816a9388)   |
| Importing functions                   | [Ex11](contracts/ex11.cairo)                          | [Link](https://testnet.starkscan.co/contract/0xab5577b9be8948d89dbdba63370a3de92e72a23c4cacaea38b3a74eec3a872)  | [Link](https://goerli.voyager.online/contract/0xab5577b9be8948d89dbdba63370a3de92e72a23c4cacaea38b3a74eec3a872)  |
| Events                                | [Ex12](contracts/ex12.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x24d15e02ddaa19d7ecd77204d35ed9bfff00a0cabc62eb3da5ba7680e44baf9) | [Link](https://goerli.voyager.online/contract/0x24d15e02ddaa19d7ecd77204d35ed9bfff00a0cabc62eb3da5ba7680e44baf9) |
| Privacy on Starknet                   | [Ex13](contracts/ex13.cairo)                          | [Link](https://testnet.starkscan.co/contract/0x2bae9190076c4252289b8a8671277cef57318192cff20c736808b0c71095895) | [Link](https://goerli.voyager.online/contract/0x2bae9190076c4252289b8a8671277cef57318192cff20c736808b0c71095895) |
| Multicall                             | [Ex14](contracts/ex14.cairo)                          | [Link](https://testnet.starkscan.co/contract/0xed7ddffe1370fbbc1974ab8122d1d9bd7e3da8d829ead9177ea4249b4caef1)  | [Link](https://goerli.voyager.online/contract/0xed7ddffe1370fbbc1974ab8122d1d9bd7e3da8d829ead9177ea4249b4caef1)  |


### 4. Counting your points and checking your progress

Your points will get credited to your installed wallet, though this may take some time. If you want to monitor your points count in real-time, you can also check your balance in a Block Explorer!
​
- Go to the  ERC20 counter on [Voyager](WIP) or [Starkscan](WIP) in the "read contract" tab.
- Enter your address in the `balanceOf` function.​

Enjoy the workshop! If you have any questions, feel free to contact us on [Discord](https://discord.gg/8Z3q3Z5). We are happy to help! 

---

## Contributing to improve this workshop

This project can be made better and will evolve. Your contributions are welcome and required! Go to the [CONTRIBUTING](CONTRIBUTING.md) file for more information on how to setup your environment and contribute to the project.

Here are **some** things that you can do to help:

- Create a branch with a translation to your language
- Correct bugs if you find some
- Add an explanation in the comments of the exercise if you feel it needs more explanation
- Add exercises showcasing your favorite Cairo feature
- Add a new tutorial to the series


## Other Automated Workshops

This workshop is the first in a series aimed at teaching how to build on Starknet. Checkout out other workshops in the series:

| Topic                                       | GitHub repo                                                                            |
| ------------------------------------------- | -------------------------------------------------------------------------------------- |
| Learn how to read Cairo code (you are here) | [Cairo 101](https://github.com/starknet-edu/starknet-cairo-101)                        |
| Deploy and customize an ERC721 NFT          | [Starknet ERC721](https://github.com/starknet-edu/starknet-erc721)                     |
| Deploy and customize an ERC20 token         | [Starknet ERC20](https://github.com/starknet-edu/starknet-erc20)                       |
| Build a cross-layer application             | [Starknet messaging bridge](https://github.com/starknet-edu/starknet-messaging-bridge) |
| Debug your Cairo contracts easily           | [Starknet debug](https://github.com/starknet-edu/starknet-debug)                       |
| Design your own account contract            | [Starknet account abstraction](https://github.com/starknet-edu/starknet-accounts)      |

### Providing feedback & getting help

Once you are done working on this tutorial, your feedback will be greatly appreciated!

**Please fill out [this form](https://forms.reform.app/starkware/untitled-form-4/kaes2e) to let us know what we can do to make it better.**

​
And if you struggle to move forward, do let us know! This workshop is meant to be as accessible as possible; we want to see if it’s not the case.
​
Do you have a question? Join our [Discord server](https://starknet.io/discord), register, and join channel #tutorials-support.

Are you interested in attending online workshops about dev on Starknet? [Subscribe here](http://eepurl.com/hFnpQ5)


## Languages

- (not updated) A Spanish version is available [here](https://github.com/starknet-edu/starknet-cairo-101/tree/spanish).
- (not updated) A Portuguese version is available [here](./README.pt.md).
- (not updated) A Korean version is available [here](./README.kr.md).