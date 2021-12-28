# Wasp-CLI Documentation

## Wasp-CLI Global Flags </br>
#### address-index </br>
`-i, --address-index int` </br>
#### config string </br>
`-c, --config string` - Path to wasp-cli.json (default wasp-cli.json)</br>
#### debug</br>
`-d, --debug`</br>
#### verbose</br>
`--verbose`</br>
#### wait</br>
`-w, --wait` - Wait for request completion (default true)</br>

## Wasp-CLI Commands</br>
#### address</br>
`./wasp-cli address` - Show the wallet address</br>
#### balance</br>
`./wasp-cli balance` - Show the wallet balance</br>
#### chain  - Interact with a chain</br>
```./wasp-cli chain activate``` - Activate the chain</br>
```./wasp-cli chain block``` - Get information about a block given its index , or latest block if missing</br>
```./wasp-cli chain call-view``` - Call a contract view function</br>
```./wasp-cli chain deactivate``` - Deactivate the chain</br>
```./wasp-cli chain deploy-contract``` - Deploy a contract in the chain</br> 
```./wasp-cli chain deposit``` - Deposit funds into on-chain account of the sender</br>
```./wasp-cli chain events``` - Show events of a contract </br>
```./wasp-cli chain info``` -  Show information about the chain</br>
```./wasp-cli chain list``` - List deployed chains</br>
```./wasp-cli chain list-accounts``` - List accounts in a chain</br>
```./wasp-cli chain list-blobs``` - List blobs in a chain</br>
```./wasp-cli chain list-contracts``` - List deployed contracts in a chain</br>
```./wasp-cli chain post-request``` - Post a request to a contract</br>
```./wasp-cli chain request``` - Get information about a request given its ID</br>
```./wasp-cli chain show-blob``` - Show a blob in the chain</br>
```./wasp-cli chain store-blob``` - Store a blob in the chain </br>

#### chain deploy - Deploy a new chain</br>
`./wasp-cli chain deploy committee ints` - subset of peers acting as committee nodes</br>
`./wasp-cli chain deploy description string` - description</br>
`./wasp-cli chain deploy peers ints` - indices of peer nodes (default: 0,1,2,3)</br>
`./wasp-cli chain deploy quorum int` - quorum of wasp nodes (default: 3)</br>
#### chain evm - Interact with EVM-Chains</br>
`./wasp-cli chain evm deploy` - Deploy the evm/evmlight chain contract</br>
`./wasp-cli chain evm jsonrpc` - Start a JSON-RPC to interact with an Ethereum Blockchain running on ISCP</br>
#### check-versions</br>
`./wasp-cli check-versions` Checks if the versions of wasp-cli and wasp nodes match</br>
#### decode</br>
`./wasp-cli decode` Decode the output of a contract function call</br>
#### help</br>
`./wasp-cli help` Help about any command</br>
#### init</br>
`./wasp-cli init` Initialize a new wallet</br>
#### metrics</br>
`./wasp-cli metrics` Show current value of collected metrics of some component</br>
#### mint</br>
`./wasp-cli mint` Mint some colored tokens</br>
#### peering</br>
`./wasp-cli peering` Configure peering</br>
#### request-funds</br>
`./wasp-cli request-funds` Request funds from the devnet faucet</br>
#### send-funds</br>
`./wasp-cli send-funds` Transfer tokens</br>
#### set</br>
`./wasp-cli set` Set a configuration value</br>
