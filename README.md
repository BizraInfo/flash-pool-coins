# Flash Pool Coins

## Purpose

The Flash Pool Coins project is designed to provide a set of mock coins for testing purposes. It includes a faucet module that allows users to request coins at specified intervals. The main features of the project include:

- Creation and management of mock coins (USDC, USDT, ETH, BTC, DAI, WING)
- Faucet functionality to distribute coins to users
- Ability to change faucet settings and deposit more coins

## Installation

To install the dependencies and build the project, follow these steps:

1. Clone the repository:
   ```
   git clone https://github.com/wing-groups/flash-pool-coins.git
   cd flash-pool-coins
   ```

2. Install the dependencies:
   ```
   aptos move install
   ```

3. Build the project:
   ```
   aptos move build
   ```

## Running Tests and Deployment

To run tests and deploy the project, follow these steps:

1. Deploy the mock coins:
   ```
   echo yes | aptos move publish --profile flashpoolcoins_test4 --package-dir ./
   ```

2. Initialize the mock coins:
   ```
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register_coins
   ```

3. Register and mint USDT:
   ```
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:100000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT
   ```

4. Register and mint USDC:
   ```
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:100000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC
   ```

5. Register and mint DAI:
   ```
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:10000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI
   ```

6. Register and mint ETH:
   ```
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:10000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
   ```

7. Register and mint BTC:
   ```
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:10000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC
   ```

8. Register and mint WING:
   ```
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:100000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING
   echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING
   ```
