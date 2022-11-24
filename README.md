for test


```
部署测试币
echo yes | aptos move publish --profile flashpoolcoins_test4 --package-dir ./

初始化测试币
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register_coins


//USDT
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:100000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDT


//USDC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:100000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::USDC


//DAI
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:10000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::DAI



//ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:10000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH



//ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:10000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::ETH



//BTC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:10000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::BTC




//WING
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::register  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::mint_coin --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 u64:100000000000000000  --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::create_faucet --args u64:10000000000000 u64:100000000000 u64:1 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING
echo yes | aptos move run --profile flashpoolcoins_test4 --function-id 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::faucet::request --args address:0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30 --type-args 0xa83690a4edb7fe646a27805b98d56bb3ddaf0983b46744e203d15e9f4dd6bf30::coins::WING

```