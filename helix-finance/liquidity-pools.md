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

flowchart
    classDef stable fill:#ggg,stroke:#EE2,stroke-width:4px;

    BTC_Helix --- MC_SWAP
    Helix --- MC_SWAP
    BSC_Helix -.- MC_SWAP
    SOL_Helix -.- MC_SWAP
    OKX_Helix -.- MC_SWAP

    SOL_Helix -.- Sol

    linkStyle 0,1,2 stroke:#940,stroke-width:3px;
    linkStyle 3,4,5 stroke:#B8F,stroke-width:2px;

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

        Helix === |45,526| wETH
        Helix --- |14,374| ETH_USDC
        DAI --- |23,665| ETH_USDC
        ETH_USDC --- |22,400| wETH
        DAI --- |28,895| wETH
        ETH_USDT --- |21,470| ETH_USDC
        wETH --- |34,583| wBTC
        TRIBE --- |690| FEI
        FXS --- |724| FRAX
        BADGER --- |1,423| Helix
        APE --- |1,491| Helix
        CULT --- |4,695| wETH
        BOND --- |786| ETH_USDC
        BAL --- |2,077| Helix
        FRAX --- |15,582| ETH_USDC
        TRIBE --- |669| Helix
    end

    subgraph Bitcoin-RSK
        RBTC(WRBTC)
        BTC_Helix(Helix)
        RIF(RIF)
        SOV(SOV)
        RUSDT((RUSDT)):::stable

        BTC_Helix --- |15,502| RBTC
        BTC_Helix --- |11,775| RUSDT
        RUSDT --- |4,384| RBTC
        RIF --- |5,754| RBTC
        SOV --- |1,451| RBTC
    end

    subgraph BSC
        BNB(BNB)
        BSC_Helix(Helix)
        BSC_CAKE(CAKE)
        BUSD((BUSD)):::stable
        BSC_USDC((USDC)):::stable
        BSC_USDT((USDT)):::stable

        BSC_Helix --- |4,155| BNB
        BSC_Helix --- |3,848| BUSD
        BNB --- |12,700| BUSD
        BSC_USDC --- |2,750| BUSD
        BUSD --- |1,200| BSC_USDT
        BSC_USDC --- |4,640| BNB
        BSC_CAKE --- |838| BNB
    end

    subgraph OKX
        OKX_Helix(Helix)
    end

    subgraph Solana
        Sol(SOL)
        SOL_Helix(Helix)
        SOL_USDC((USDC)):::stable
        SOL_USDT((USDT)):::stable
    end
```

Reference Quotes:

- *"yes that's right.. you'll be able to move HELIX from Bitcoin to Ethereum to Solana to BSC by the end of the expansion, each network will have HELIX-WETH, or HELIX-RBTC, or HELIX-SOL, or HELIX-BNB you'll be able to then enter that market via"* ([link](https://discord.com/channels/894851963483750430/894855639942176799/1002198215560544307))
