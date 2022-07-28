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
        A === |large-pool| B
        A --- |small-pool| C
        C -.- |unlisted-pool| B
        C -.- |same token| D

        linkStyle 3 stroke:#BBF,stroke-width:2px;
    end
```

___

```mermaid

flowchart BT
    classDef stable fill:#ggg,stroke:#EE2,stroke-width:4px;

    BTC_Helix -.- MC_SWAP
    Helix -.- MC_SWAP
    BSC_Helix -.- MC_SWAP
    SOL_Helix -.- MC_SWAP

    wBTC -.- BTC
    SOL_Helix -.- Sol
    BSC_Helix -.- BNB
    BTC_Helix -.- BTC

    linkStyle 0,1,2,3,4,5,6,7 stroke:#BBF,stroke-width:2px;

    subgraph -MULTICHAIN-
        MC_SWAP(Multichain Bridge)
    end        

    subgraph Ethereum
        wETH(wETH)
        wBTC(wBTC)
        Helix(HELIX)
        TRIBE(TRIBE)
        FEI(FEI)
        FXS(FXS)
        FRAX(FRAX)
        BADGER(BADGER)
        APE(APE)
        CULT(CULT)
        BOND(BOND)
        BAL(BAL)
        ETH_USDC((USDC)):::stable
        ETH_USDT((USDT)):::stable
        DAI((DAI)):::stable
        Helix === |75,800| wETH
        Helix --- |26,624| ETH_USDC
        DAI --- |19,490| ETH_USDC
        ETH_USDC --- |21,400| wETH
        DAI --- |21473| wETH
        ETH_USDT --- |25,937| ETH_USDC
        wETH --- |319| wBTC
        TRIBE --- |338| FEI
        FXS --- |374| FRAX
        BADGER --- |615| Helix
        APE --- |1,164| Helix
        CULT --- |1,897| wETH
        BOND --- |100| ETH_USDC
        BAL --- |330| Helix
    end

    subgraph Bitcoin
        BTC(BTC)
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
