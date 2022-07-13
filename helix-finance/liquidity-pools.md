Keeping track of liquidity pool size and paths here to identify optimal routes.

* [Link to LP Farms](https://helix.finance/farms)
* [Mermaid Online Editor](https://mermaid.live/edit#pako:eNqNkm1vgjAQx79KU9_UpCzOqUgXX4iQuGTRZLh3JEuF8hALGCjRRfzuK-ADU7bYpNf27tf_XS89QCdxGSTQ48nOCWgq7BjI4XCaZQbzQCbomjPghZyTju_7OBNpsmGkY5r9017Zha4IyGC7f7Xj-nqWr_2UbgNgioClLI9qdzl25mqOStO9-uaMh3tU2YZXMl-fljFDqLTdLiGkruYOWVXIqhUxpm8ISdMarFKCyWQCiqGGR72x9BVVib8EgPKkgELD6lgrLmXdFwoURWIqVtXnVpEyOsY9dXgbPT-jzjPAI210m4fF7l1zrYTTmF5l5BlZy_dGC-Xpvxa2iepW42X6QkdyNhT1Wq5cHpJbmNOPv6PL8nuAWUDDGPQfw14uGMQwYmlEQ1f-30PptqEEI2ZDIrcuTTc2tOOj5PKtSwUz3VAkKSQe5RnDkOYisb5jBxKR5uwMGSGVSaMTdfwBo0rmMQ)

```mermaid
flowchart
    classDef stable fill:#ggg,stroke:#EE2,stroke-width:4px;

    subgraph Ethereum
        wETH(wETH)
        Helix(Helix)
        ETH_USDC((USDC)):::stable
        ETH_USDT((USDT)):::stable
        DAI((DAI)):::stable
        Helix === |59,608   | wETH
        DAI -.- |9,789| ETH_USDC
        ETH_USDC --- |7,771| wETH
        DAI --- |8,075| wETH
        ETH_USDT -.- |4,696| ETH_USDC
    end

    subgraph Solana
        Sol(SOL)
        SOL_USDC((USDC)):::stable
    end

    subgraph BSC
        BNB(BNB)
        BUSDC((BUSD)):::stable
    end

    subgraph NEAR
    end

    subgraph Other Chain 2
    end

    subgraph Other Chain 3
    end
```
