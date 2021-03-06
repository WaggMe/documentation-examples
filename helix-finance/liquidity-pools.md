Keeping track of liquidity pool size and paths here to identify optimal routes.

* [Link to LP Farms](https://helix.finance/farms)
* [Mermaid Online Editor](https://mermaid.live/edit#pako:eNqNkm1vgjAQx79KU9_UpCzOqUgXX4iQuGTRZLh3JEuF8hALGCjRRfzuK-ADU7bYpNf27tf_XS89QCdxGSTQ48nOCWgq7BjI4XCaZQbzQCbomjPghZyTju_7OBNpsmGkY5r9017Zha4IyGC7f7Xj-nqWr_2UbgNgioClLI9qdzl25mqOStO9-uaMh3tU2YZXMl-fljFDqLTdLiGkruYOWVXIqhUxpm8ISdMarFKCyWQCiqGGR72x9BVVib8EgPKkgELD6lgrLmXdFwoURWIqVtXnVpEyOsY9dXgbPT-jzjPAI210m4fF7l1zrYTTmF5l5BlZy_dGC-Xpvxa2iepW42X6QkdyNhT1Wq5cHpJbmNOPv6PL8nuAWUDDGPQfw14uGMQwYmlEQ1f-30PptqEEI2ZDIrcuTTc2tOOj5PKtSwUz3VAkKSQe5RnDkOYisb5jBxKR5uwMGSGVSaMTdfwBo0rmMQ)

___

```mermaid


flowchart
    classDef stable fill:#ggg,stroke:#EE2,stroke-width:4px;

    subgraph Legend-1
        token(native coin)
        stable((stablecoin)):::stable
        end
    
    subgraph Legend-2
        A(A)
        B(B)
        C((C)):::stable
        D((D)):::stable
        E(E)
        A === |large-pool| B
        A --- |small-pool| C
        C -.- |unlisted-pool| B
        C -.- |same token| D
        B --- |external platform| E
        D --- |external platform| E

        linkStyle 3 stroke:#B8F,stroke-width:2px;
        linkStyle 4,5 stroke:#940,stroke-width:3px;
    end
```

___

```mermaid

flowchart BT
    classDef stable fill:#ggg,stroke:#EE2,stroke-width:4px;

    BTC_Helix --- MC_SWAP
    Helix --- MC_SWAP
    BSC_Helix -.- MC_SWAP
    SOL_Helix -.- MC_SWAP

    wBTC -.- BTC
    SOL_Helix -.- Sol
    BSC_Helix -.- BNB
    BTC_Helix -.- BTC

    linkStyle 0,1 stroke:#940,stroke-width:3px;
    linkStyle 2,3,4,5,6,7 stroke:#B8F,stroke-width:2px;

    subgraph -MULTICHAIN-
        MC_SWAP(Multichain Bridge)
    end        

    subgraph Ethereum
        
        subgraph ETH-Stables
            ETH_USDT((USDT)):::stable
            DAI((DAI)):::stable
            ETH_USDC((USDC)):::stable
        end
        
        wETH(wETH)
        wBTC(wBTC)
        Helix(HELIX)
        FXS(FXS)
        FRAX(FRAX)
        BADGER(BADGER)
        TRIBE(TRIBE)
        FEI(FEI)
        APE(APE)
        CULT(CULT)
        BOND(BOND)
        BAL(BAL)

        Helix === |76,140| wETH
        Helix --- |29,986| ETH_USDC
        DAI --- |19,651| ETH_USDC
        ETH_USDC --- |21,654| wETH
        DAI --- |21,253| wETH
        ETH_USDT --- |20,252| ETH_USDC
        wETH --- |970| wBTC
        TRIBE --- |338| FEI
        FXS --- |724| FRAX
        BADGER --- |602| Helix
        APE --- |536| Helix
        CULT --- |1,640| wETH
        BOND --- |847| ETH_USDC
        BAL --- |2,141| Helix
        FRAX --- |122| ETH_USDC
        TRIBE --- |154| Helix
    end

    subgraph Bitcoin-RSK
        BTC(RBTC)
        BTC_Helix(Helix)
    end

    subgraph Solana
        Sol(SOL)
        SOL_Helix(Helix)
        SOL_USDC((USDC)):::stable
        SOL_USDT((USDT)):::stable
    end

    subgraph BSC
        BNB(BNB)
        BSC_Helix(Helix)
        BUSDC((BUSD)):::stable
    end
```

Reference Quotes:

- *"yes that's right.. you'll be able to move HELIX from Bitcoin to Ethereum to Solana to BSC by the end of the expansion, each network will have HELIX-WETH, or HELIX-RBTC, or HELIX-SOL, or HELIX-BNB you'll be able to then enter that market via"* ([link](https://discord.com/channels/894851963483750430/894855639942176799/1002198215560544307))
