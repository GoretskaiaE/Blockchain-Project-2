# Decentralized Star Notary Service Project

RC-721 Token Name: Cool Star Token

ERC-721 Token Symbol: CST

“Token Address” on the Rinkeby Network: 0x42a0F89492E94f3f41bb267cDd10673b542398d1

Truffle version: v5.4.12

OpenZeppelin version: 2.3

Solidity v0.5.16 (solc-js)

Node v10.16.3

Web3.js v1.5.3


Perhaps you'll want to use Node Version Manager to switch between multiple Node.js versions.
Follow the useful guide to install NodeJS on Windows https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-windows
Node Version Manager for unix, macOS is here https://github.com/nvm-sh/nvm

Follow instructions https://github.com/udacity/nd1309-p2-Decentralized-Star-Notary-Service-Starter-Code#dependencies to install all needed packages.

## Troubleshoot
#### Error
In VS Code truffle version command leads to error "truffle : Impossible to load file..."
**Solution:**
Check PowerShell execution policies https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies
Examples:
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Set-ExecutionPolicy -ExecutionPolicy Restricted -Scope CurrentUser


## How to test locally
Open Ganashe

```bash
truffle migrate
truffle test

cd app
npm run dev
```

Open http://localhost:8080/ in browser with installed Metamask 

Import an account from Ganashe to Metamask
Connect the account to http://localhost:8080/ in Metamask

On http://localhost:8080/ 
insert Star Name, Star ID
click button 'Create Star'
confirm transaction in Metamask


insert Star ID of created star in field under 'Look up a Star' header
click button 'Look Up a Star'


## How to deploy ERC721 Token Contract on Rinkeby
Follow the instructions 
https://classroom.udacity.com/nanodegrees/nd1309/parts/409a9bed-96ac-45ea-8a7f-834a4898b02e/modules/b462eb33-099b-4d57-b00e-5200ae6d8634/lessons/70703034-f10d-45a9-9979-fa8afc8ea42c/concepts/84d298b9-f5bc-4c46-9fd3-1070235d518f

My contract https://rinkeby.etherscan.io/address/0x42a0f89492e94f3f41bb267cdd10673b542398d1

Run Dapp
```bash
cd app
npm run dev
```

Open http://localhost:8080/ in browser with installed Metamask 
Select Rinkeby Test Network

Create star!

Read this https://metamask.zendesk.com/hc/en-us/articles/360058238591 to know more about NFT tokens in MetaMask wallet.


## Appendix
Output after truffle migrate --reset --network rinkeby
```bash
Migrations dry-run (simulation)
===============================
> Network name:    'rinkeby-fork'
> Network id:      4
> Block gas limit: 29970705 (0x1c95111)


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > block number:        9370080
   > block timestamp:     1632808271
   > account:             0xAd667ae1d274f9872c2f0A46e2c23C7744AdBcC3
   > balance:             2.99770364
   > gas used:            229636 (0x38104)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00229636 ETH

   -------------------------------------
   > Total cost:          0.00229636 ETH


2_deploy_contracts.js
=====================

   Deploying 'StarNotary'
   ----------------------
   > block number:        9370082
   > block timestamp:     1632808286
   > account:             0xAd667ae1d274f9872c2f0A46e2c23C7744AdBcC3
   > balance:             2.97519571
   > gas used:            2223419 (0x21ed3b)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.02223419 ETH

   -------------------------------------
   > Total cost:          0.02223419 ETH


Summary
=======
> Total deployments:   2
> Final cost:          0.02453055 ETH





Starting migrations...
======================
> Network name:    'rinkeby'
> Network id:      4
> Block gas limit: 29999943 (0x1c9c347)


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0xedf092f63a3e437bafb0b56353269be5f3d57a7e725718c83aaaab0a67c4d1c9
   > Blocks: 1            Seconds: 13
   > contract address:    0x9Ed488B06d7Fe68a91C2f17032168cDde3EA6266
   > block number:        9370082
   > block timestamp:     1632808312
   > account:             0xAd667ae1d274f9872c2f0A46e2c23C7744AdBcC3
   > balance:             2.99754064
   > gas used:            245936 (0x3c0b0)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00245936 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00245936 ETH


2_deploy_contracts.js
=====================

   Deploying 'StarNotary'
   ----------------------
   > transaction hash:    0x16f94cdd956379cb8e077d92b3dcd442efd6cf1ff11887591745d8af53d1cc9f
   > Blocks: 1            Seconds: 9
   > contract address:    0x42a0F89492E94f3f41bb267cDd10673b542398d1
   > block number:        9370084
   > block timestamp:     1632808342
   > account:             0xAd667ae1d274f9872c2f0A46e2c23C7744AdBcC3
   > balance:             2.97452271
   > gas used:            2256019 (0x226c93)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.02256019 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.02256019 ETH


Summary
=======
> Total deployments:   2
> Final cost:          0.02501955 ETH
```