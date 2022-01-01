# Wasp-CLI Documentation

* [Global Flags](#global-flags)
  * [address-index](#address-index)
  * [config string](#config-string)
  * [debug](#debug)
  * [verbose](#verbose)
  * [wait](#wait)
  * [help](#help)
* [Wasp-CLI Commands](#wasp-cli-commands)
  * [address](#address)
  * [balance](#balance)
  * [chain](#chain)
    * [activate](#activate)
    * [block](#block)
    * [call-view](#call-view)
    * [deactivate](#deactivate)
    * [deploy](#deploy)
      * [committee](#committee)
      * [description](#description)
      * [peers](#peers)
      * [quorum](#quorum)
    * [deploy-contract](#deploy-contract)
    * [deposit](#deposit)
    * [events](#events)
    * [info](#info)
    * [list](#list)
    * [list-accounts](#list-accounts)
    * [list-blobs](#list-blobs)
    * [list-contracts](#list-contracts)
    * [request](#request)
    * [post-request](#post-request)
    * [show-blob](#show-blob)
    * [store-blob](#store-blob)
  * [check-versions](#check-versions)
  * [decode](#decode)
  * [init](#init)
  * [metrics](#metrics)
  * [mint](#mint)
  * [peering](#peering)
  * [request-funds](#request-funds)
  * [send-funds](#send-funds)
  * [set](#set)


<!-- Global Flags  -->
## Global Flags
* #### address-index 
    Add an address-index to your command
    <details>
    <summary>Example</summary>

    Command:

    ```bash
    ./wasp-cli address
    ./wasp-cli address -i 5
    ```

    Response:

    ```bash
    Address index 0
      Address:     1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu

    Address index 5
      Address:     1HCFjRdyMMZBDTV4vAptdtgLYVixoZYmoBmPk6Hg2Nyko
    ```

    </details>
    
* #### config-string
    Provide the path to your wasp-cli.json (default: **./wasp-cli.json**)
    <details>
    <summary>Example</summary>

    Example:

    ```bash
    root@iota-defi-sc:/opt/services/iscp/deps/wasp-cli# ls
    docker-entrypoint.sh  Dockerfile  wasp-cli
    root@iota-defi-sc:/opt/services/iscp/deps/wasp-cli# ./wasp-cli -c ../../data/     wasp-cli.json address
    Address index 0
      Address:     1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu

    ```

    </details>

* #### debug
    Enable debug information
    <details>
    <summary>Example</summary>
    
    ```bash
    ./wasp-cli --debug
    ./wasp.cli -d
    ```

    </details>

* #### verbose
    be verbose
    <details>
    <summary>Example</summary>
    
    Example

    ```bash
    ./wasp-cli address --verbose
    Address index 0
      Private key: 3y2qamP4KLsedUbfABawtUYw8HGduqstQXgLaAFfo2uFXZAedZXvC5TwdSBBKbYHs4WyiPkfk7kvSqpsNSh1gZy
      Public key:  64iDMsPDYb2YYFhpRJxkPRvdgEPBe5etBvux4rCohj3y
      Address:     1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu

    Instead of:
    ./wasp-cli address
    Address index 0
      Address:     1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu  
    ```

    </details>

* #### wait
    wait for request completion (default: **true**)
    

* #### help
    help for wasp-cli
    <details>
    <summary>Example</summary>
    
    ```bash
        ./wasp-cli -h
    ```

    </details>

## Wasp-CLI-Commands

* #### address
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli address
    ```
    
    Response:

    ```bash
    Address index -i 1
    Address:     1BKQi3aa998nLP5be2KSi79GdcZSHN6v8mLFPQmDR2DbT  
    ```
    
    </details>

* #### balance
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli balance -i 1
    ```

    Response:

    ```bash
    Address index 1
        Address: 1BKQi3aa998nLP5be2KSi79GdcZSHN6v8mLFPQmDR2DbT
        Balance:
        IOTA: 989898
        ---------------------------------------------------------
        Total: 989898
    ```

    </details>

* #### chain

    * #### activate
        
        <details>
        <summary>Example</summary>
    
        Command:

        ```bash
        ./wasp-cli chain activate --verbose
        ```

        Response:

        ```bash
        using Wasp host https://api.wasp.sc.iota.org
        ```

        </details>

    * #### block
        
        <details>
        <summary>Example</summary>
    
        Command:

        ```bash
        ./wasp-cli chain block
        ```

        Response:

        ```bash
        Block index: 235
        Timestamp: 2021-12-29T08:39:13Z
        Total requests: 1
        Successful requests: 1
        Off-ledger requests: 0
        Request 0 (5tKCDwpGkNcJzFMjkTqY4rJvfiX6TYaUCSVvSaMG5hgbV9)
            Kind: on-ledger
            Fee prepaid: no
            Sender: A/rrP4KDUsrEmuR4WaRYdWUH184ARTq9amaJBMV3vJHpbY::22e87e2d
            Contract Hname: 22e87e2d
            Entry point: b9c353a4
            Timestamp: 2021-12-29T08:39:10Z
            Arguments: (empty)
            Error: (empty)

        Total 0 events

        ```

        </details>

    * #### call-view

         <details>
        <summary>Example</summary>
    
        Command:

        ```bash
        
        ```

        Response:

        ```bash
        
        ```

        </details>

   * #### deactivate
        
        <details>
        <summary>Example</summary>
    
        Command:

        ```bash
        ./wasp-cli chain deactivate --verbose
        ```

        Response:

        ```bash
        using Wasp host https://api.wasp.sc.speccers-mana-fountain.org
        ```

        </details>

    * #### deploy

        * ##### committee
            
            <details>
            <summary>Example</summary>
    
            Command:

            ```bash
            ./wasp-cli chain deploy --committee=0,1,2,3 
            ```

            Response:

            ```bash
            creating new chain. Owner address: 1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu. 
            State controller: UKkyiXTxSNxdr5aevmmcUDvBBfiFgCadYffETd84Bwct, N = 1, T = 3
            creating chain origin and init transaction 3Ld5XwiohBRCaRFXS6vGDJKtxpu2sJDNLoWSdpq6q5n6.. OK
            sending committee record to nodes.. OK
            activating chain ff8ZUUNKj755YxZghNpKa7KN3rGXUqUWdrssBJjHx8xP.. OK.
            chain has been created successfully on the Tangle. 
            ChainID: $/ff8ZUUNKj755YxZghNpKa7KN3rGXUqUWdrssBJjHx8xP, State address: UKkyiXTxSNxdr5aevmmcUDvBBfiFgCadYffETd84Bwct, N = 1, T = 3
            ```

            ![Chain deploy](img/chain-deploy.jpg)

            </details>

        * ##### description
            
            <details>
            <summary>Example</summary>
    
            Command:

            ```bash
            ./wasp-cli chain deploy --committee=0 --quorum=1 --description="DokuChain"
            ```

            Response:

            ```bash
            creating new chain. Owner address: 1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu. 
            State controller: Zf3nfAKAZqjowZQ5rZhwNwX9AHF28vgBgiLFJPHjt1Xh, N = 1, T = 1
            creating chain origin and init transaction 7kGp7Fkdn5c4dehuaZChaKzeqgwQAmxGiDJFCQvtL7FV.. OK
            sending committee record to nodes.. OK
            activating chain kf3YnVTbEgEAjyK5thXuaH61AdZmDs6Qttn7gjzG9H4k.. OK.
            chain has been created successfully on the Tangle.
            ChainID: $/kf3YnVTbEgEAjyK5thXuaH61AdZmDs6Qttn7gjzG9H4k, State address: Zf3nfAKAZqjowZQ5rZhwNwX9AHF28vgBgiLFJPHjt1Xh, N = 1, T = 1

            ```

            ![Chain deploy](img/chain-deploy.jpg)

            </details>

        * ##### peers
            
            <details>
            <summary>Example</summary>
    
            Command:

            ```bash
        
            ```

            Response:

            ```bash
        
            ```

            </details>

        * ##### quorum
            
            <details>
            <summary>Example</summary>
    
            Command:

            ```bash
        
            ```

            Response:

            ```bash
        
            ```

            </details>

  * ##### deploy-contract
    
    <details>
    <summary>Example</summary>
    
    ```bash

    ```

    Response:

    ```bash
    
    ```

    </details>

  * ##### deposit
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli chain deposit IOTA:100
    ```

    Response:

    ```bash
    Posted on-ledger transaction 5KZgzDM93AtNtcHEmvQovD7skwRWTFwQ75mh3i353LY8 containing 1 request:
    -  (check result with: ./wasp-cli chain request 2TANbnucWCjTHvxnvFEVBSRS7RYGj8YDoPuXN8zJVaFTyEX)
    Waiting for tx requests to be processed...    
    ```

    </details>

  * ##### events
    
    <details>
    <summary>Example</summary>
    
     ```bash

    ```

    Response:

    ```bash
    
    ```

    </details>

  * ##### info
    
    <details>
    <summary>Example</summary>

    Command:

    ```bash
    ./wasp-cli chain info
    ```

    Response:

    ```bash
    Chain ID: kAGLveDrYceD8j46M6rh5udMR6N2E7HkxraRhT1LJT4N
    Committee nodes: [127.0.0.1:4000]
    Active: true
    Description: Test EVM
    #Contracts: 7
    Owner: A/1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu::00000000
    Default owner fee: 0 IOTA
    Default validator fee: 0 IOTA
    ```

    </details>

  * ##### list
    
    <details>
    <summary>Example</summary>

    Command:

    ```bash
    ./wasp-cli chain list
    ```

    Response:

    ```bash
    Total 1 chain(s) in wasp node https://api.wasp.sc.iota-defi.com
    -------                                       ------
    chainid                                       active
    -------                                       ------
    kAGLveDrYceD8j46M6rh5udMR6N2E7HkxraRhT1LJT4N  true
    ```

    </details>

  * ##### list-accounts
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli chain list-accounts
    ```

    Response:

    ```bash
    Total 3 account(s) in chain kAGLveDrYceD8j46M6rh5udMR6N2E7HkxraRhT1LJT4N
    -------
    agentid
    -------
    A/kAGLveDrYceD8j46M6rh5udMR6N2E7HkxraRhT1LJT4N::adc164b5
    A/1HxJxu91B5txjaCQZCrxKEYL2BBxditP9JXQ61z46eJRu::00000000
    A/kAGLveDrYceD8j46M6rh5udMR6N2E7HkxraRhT1LJT4N::00000000
    ```

    </details>
  
  * ##### list-blobs
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli chain list-blobs
    ```

    Response:

    ```
    Total 0 blob(s) in chain $/kAGLveDrYceD8j46M6rh5udMR6N2E7HkxraRhT1LJT4N
    ```

    </details>

  * ##### list-contracts
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli chain list-contracts
    ```

    Response:

    ```bash
    Total 7 contracts in chain $/kAGLveDrYceD8j46M6rh5udMR6N2E7HkxraRhT1LJT4N
    -----     ----        -----------                    --------                                      -------                                                    ---------                           -------------
    hname     name        description                    proghash                                      creator                                                    owner fee                           validator fee
    -----     ----        -----------                    --------                                      -------                                                    ---------                           -------------
    cebf5908  root        Root Contract                  ZbduPgjygsVS4Pvc9s34xUn9u3JsVw1yyqTY57Ub2uW   A/111111111111111111111111111111111::00000000              0   0
    f538ef2b  blocklog    Block log contract             3xW6qNoMyETgBcYHede5Cju8nZ1Eyt27hoxPhDyXHWac  A/111111111111111111111111111111111::00000000              0   0
    fd91bc63  blob        Blob Contract                  7iL8ojzK47m2KVYpNPMc7BSt6tWxCfF4xefYB2tdTkKs  A/111111111111111111111111111111111::00000000              0   0

    ```

    </details>

  * ##### post-request
    
    <details>
    <summary>Example</summary>
    
    ```bash

    ```

    Response:

    ```bash
    
    ```

    </details>
  
  * ##### request
    
    <details>
    <summary>Example</summary>
    
    ```bash

    ```

    Response:

    ```bash
    
    ```

    </details>
  
  * ##### show-blob
    
    <details>
    <summary>Example</summary>
    
    ```bash

    ```

    Response:

    ```bash
    
    ```

    </details>

  * ##### store-blob
    
    <details>
    <summary>Example</summary>
    
    ```bash

    ```

    Response:

    ```bash
    
    ```

    </details>

* #### check-versions
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli check-versions
    ```
    
    Response:

    ```bash
    Wasp-cli version matches Wasp #0
    ```
    
    </details>

* #### decode
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli 
    ```
    
    Response:

    ```bash
  
    ```
    
    </details>

* #### init
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli init
    ```
    
    Response:

    ```bash
    Initialized wallet seed in wasp-cli.json

    IMPORTANT: wasp-cli is alpha phase. The seed is currently being stored in a plain text file which is NOT secure. Do not use this seed to store funds in the mainnet!
    ```
    
    </details>

* #### metrics
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli 
    ```
    
    Response:

    ```bash
  
    ```
    
    </details>

* #### mint
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli mint 10
    ```
    
    Response:

    ```bash
    Posted on-ledger transaction 6NxAa3HajLbP7AY2satganyqk8GmZ377kSfT8nXkZdC
    Minted 10 tokens of color 3bdu2XjVePNJ8MB5oGHCHU8RPvjPeV8SpbE6RHLt5DXU
    Transaction ID: 6NxAa3HajLbP7AY2satganyqk8GmZ377kSfT8nXkZdC
    ```
    
    </details>

* #### peering
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```bash
    ./wasp-cli 
    ```
    
    Response:

    ```bash
  
    ```
    
    </details>

* #### request-funds
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```
    ./wasp-cli request-funds 
    ```
    
    Response:

    ```
    Request funds for address 1BKQi3aa998nLP5be2KSi79GdcZSHN6v8mLFPQmDR2DbT: success
    ```
    
    </details>

* #### send-funds
    
    <details>
    <summary>Example</summary>
    
    Command:

    ```
    ./wasp-cli send-funds 14zg9ynYZLTVnd1SPxrqCuTLdTGVkU8cz6cskAevRMVHm 
    ```
    
    Response:

    ```bash
  
    ```
    
    </details>

* #### set
    
    <details>
    <summary>Example</summary>
    
    Example wasp-cli.json:

    ```bash
    wasp-cli set goshimmer.api 127.0.0.1:8080

    wasp-cli set wasp.0.api 127.0.0.1:9090
    wasp-cli set wasp.0.nanomsg 127.0.0.1:5550
    wasp-cli set wasp.0.peering 127.0.0.1:4000

    ## You can add as many nodes as you like in your committee
    wasp-cli set wasp.1.api 127.0.0.1:9091
    wasp-cli set wasp.1.nanomsg 127.0.0.1:5551
    wasp-cli set wasp.1.peering 127.0.0.1:4001

    ...

    wasp-cli set wasp.N.api 127.0.0.1:9091
    wasp-cli set wasp.N.nanomsg 127.0.0.1:5551
    wasp-cli set wasp.N.peering 127.0.0.1:4001
    ```
    
    </details>
