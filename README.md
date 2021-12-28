# Wasp-CLI Documentation

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ul>
    <li>
      <a href="#Wasp-CLI Global Flags">Wasp-CLI Global Flags</a>
      <ul>
        <li><a href="#address-index">address index</a></li>
        <li><a href="#config string">config string</a></li>
        <li><a href="#debug">debug</a></li>
        <li><a href="#verbose">verbose</a></li>
        <li><a href="#wait">wait</a></li>
      </ul>
    </li>
    <li>
      <a href="#Wasp-CLI Commands">Wasp-CLI Commands</a>
      <ul>
        <li><a href="#address">address</a></li>
        <li><a href="#balance">balance</a></li>
        <li><details>
            <summary>chain</summary>
            <ul>
                <li><a href="#activate">activate</a></li>
                <li><a href="#balance">balance</a></li>
                <li><a href="#block">block</a></li>
                <li><a href="#call-view">call-view</a></li>
                <li><a href="#deactivate">deactivate</a></li>
                <li><details>
                    <summary>deploy</summary>
                    <ul>
                      <li><a href="#committe">committee</a></li>
                      <li><a href="#description">description</a></li>
                      <li><a href="#peers">peers</a></li>
                      <li><a href="#quorum">quorum</a></li>
                    </ul>
                    </details>
                </li>
                <li><a href="#deploy-contract">deploy-contract</a></li>
                <li><a href="#deposit">deposit</a></li>
                <li><a href="#events">events</a></li>
                <li><details>
                    <summary>evm</summary>
                    <ul>
                      <li><a href="#deploy">deploy</a></li>
                      <li><a href="#jsonrpc">jsonrpc</a></li>
                    </ul>
                    </details>
                </li>
                <li><a href="#info">info</a></li>
                <li><a href="#list">list</a></li>
                <li><a href="#list-accounts">list-accounts</a></li>
                <li><a href="#list-blobs">list-blobs</a></li>
                <li><a href="#list-contracts">list-contracts</a></li>
                <li><a href="#post-request">post-request</a></li>
                <li><a href="#request">request</a></li>
                <li><a href="#show-blob">show-blob</a></li>
                <li><a href="#store-blob">store-blob</a></li>
            </ul>
            </details></li>
        <li><a href="#check-versions">check-versions</a></li>
        <li><a href="#decode">decode</a></li>
        <li><a href="#help">help</a></li>
        <li><a href="#init">init</a></li>
        <li><a href="#metrics">metrics</a></li>
        <li><a href="#mint">mint</a></li>
        <li><a href="#peering">peering</a></li>
        <li><a href="#request-funds">request-funds</a></li>
        <li><a href="#send-funds">send-funds</a></li>
        <li><a href="#set">set</a></li>
      </ul>
    </li>

  </ul>
</details>


## Wasp-CLI Global Flags
#### address-index
`-i, --address-index int`
#### config string
`-c, --config string` - Path to wasp-cli.json (default wasp-cli.json)
#### debug
`-d, --debug`
#### verbose
`--verbose`
#### wait
`-w, --wait` - Wait for request completion (default true)


## Wasp-CLI Commands
#### address
`./wasp-cli address` - Show the wallet address
#### balance
`./wasp-cli balance` - Show the wallet balance
#### chain  - Interact with a chain
`./wasp-cli chain activate` - Activate the chain
`./wasp-cli chain block` - Get information about a block given its index , or latest block if missing
`./wasp-cli chain call-view` - Call a contract view function
`./wasp-cli chain deactivate` - Deactivate the chain
`./wasp-cli chain deploy-contract` - Deploy a contract in the chain 
`./wasp-cli chain deposit` - Deposit funds into on-chain account of the sender
`./wasp-cli chain events` - Show events of a contract 
`./wasp-cli chain info` -  Show information about the chain
`./wasp-cli chain list` - List deployed chains
`./wasp-cli chain list-accounts` - List accounts in a chain
`./wasp-cli chain list-blobs` - List blobs in a chain
`./wasp-cli chain list-contracts` - List deployed contracts in a chain
`./wasp-cli chain post-request` - Post a request to a contract
`./wasp-cli chain request` - Get information about a request given its ID
`./wasp-cli chain show-blob` - Show a blob in the chain
`./wasp-cli chain store-blob` - Store a blob in the chain 

#### chain deploy - Deploy a new chain
`./wasp-cli chain deploy committee ints` - subset of peers acting as committee nodes
`./wasp-cli chain deploy description string` - description
`./wasp-cli chain deploy peers ints` - indices of peer nodes (default: 0,1,2,3)
`./wasp-cli chain deploy quorum int` - quorum of wasp nodes (default: 3)
#### chain evm - Interact with EVM-Chains
`./wasp-cli chain evm deploy` - Deploy the evm/evmlight chain contract
`./wasp-cli chain evm jsonrpc` - Start a JSON-RPC to interact with an Ethereum Blockchain running on ISCP
#### check-versions
`./wasp-cli check-versions` Checks if the versions of wasp-cli and wasp nodes match
#### decode
`./wasp-cli decode` Decode the output of a contract function call
#### help
`./wasp-cli help` Help about any command
#### init
`./wasp-cli init` Initialize a new wallet
#### metrics
`./wasp-cli metrics` Show current value of collected metrics of some component
#### mint
`./wasp-cli mint` Mint some colored tokens
#### peering
`./wasp-cli peering` Configure peering
#### request-funds
`./wasp-cli request-funds` Request funds from the devnet faucet
#### send-funds
`./wasp-cli send-funds` Transfer tokens
#### set
`./wasp-cli set` Set a configuration value
