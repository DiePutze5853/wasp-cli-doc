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
`./wasp-cli chain activate` - Activate the chain</br>
`./wasp-cli chain block` - Get information about a block given its index , or latest block if missing</br>
`./wasp-cli chain call-view` - Call a contract view function</br>
`./wasp-cli chain deactivate` - Deactivate the chain</br>
`./wasp-cli chain deploy-contract` - Deploy a contract in the chain</br> 
`./wasp-cli chain deposit` - Deposit funds into on-chain account of the sender</br>
`./wasp-cli chain events` - Show events of a contract </br>
`./wasp-cli chain info` -  Show information about the chain</br>
`./wasp-cli chain list` - List deployed chains</br>
`./wasp-cli chain list-accounts` - List accounts in a chain</br>
`./wasp-cli chain list-blobs` - List blobs in a chain</br>
`./wasp-cli chain list-contracts` - List deployed contracts in a chain</br>
`./wasp-cli chain post-request` - Post a request to a contract</br>
`./wasp-cli chain request` - Get information about a request given its ID</br>
`./wasp-cli chain show-blob` - Show a blob in the chain</br>
`./wasp-cli chain store-blob` - Store a blob in the chain </br>

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
`./wasp-cli set` Set a configuration value
