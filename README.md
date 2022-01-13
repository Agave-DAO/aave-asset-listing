# Agave Governance V2: Listing a new asset

This repository facilitates the last step of the process of listing a new asset to the Agave protocol, that is creating the on-chain proposal to the Agave Governance.

## Requirements 
Following the
- You must have deployed the AToken, VariableDebtToken, StableDebtToken, InterestStrategy overlying contracts for your token.

## Set the environment variables.

Copy the `.default.env` file, rename it to `.env` and update it to match with your tokens addresses and your risk parameters.

Example for the GNO Token listing: 

```
## You need either an infura or alchemy key with archive node setup
INFURA_KEY= XXX
ALCHEMY_KEY= XXX
MNEMONIC= XXX
TOKEN=0xA91B9095eFa6C0568467562032202108e49c9Ef8
ATOKEN=0x446174992Caaa9505DE55eE21D07754eC9c25E72
STABLE_DEBT_TOKEN=0xf3779f51B26910A75150999D3517B5360232bB6c
VARIABLE_DEBT_TOKEN=0x6E2Ead844b785A5f44290066ea0EE44338511464
INTEREST_STRATEGY=0xF4440Eb6B91103feEEBCD4aa2Cb32DC52F8C71D5
LTV=5500
LIQUIDATION_THRESHOLD=6500
LIQUIDATION_BONUS=11000
RESERVE_FACTOR=2000
DECIMALS=18
ENABLE_AS_COLLATERAL=true
ENABLE_BORROW=true
ENABLE_STABLE_BORROW=false
```
# Node
## Install

`$ npm i`

## Run the test

`$ npm run test`
## Run the deployment script

`$ npm run propose-new-asset:gnosis` for gnosis chain

# docker-compose

In one terminal tab: `docker-compose up`

Enter the container in new tab: `docker-compose exec contracts-env bash`

In the container run: 

`$ npm run test`

`$ npm run propose-new-asset:gnosis` for gnosis chain


