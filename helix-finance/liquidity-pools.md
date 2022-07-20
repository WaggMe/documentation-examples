Keeping track of liquidity pool size and paths here to identify optimal routes.

* [Link to LP Farms](https://helix.finance/farms)
* [Mermaid Online Editor](https://mermaid.live/edit#pako:eNqNkm1vgjAQx79KU9_UpCzOqUgXX4iQuGTRZLh3JEuF8hALGCjRRfzuK-ADU7bYpNf27tf_XS89QCdxGSTQ48nOCWgq7BjI4XCaZQbzQCbomjPghZyTju_7OBNpsmGkY5r9017Zha4IyGC7f7Xj-nqWr_2UbgNgioClLI9qdzl25mqOStO9-uaMh3tU2YZXMl-fljFDqLTdLiGkruYOWVXIqhUxpm8ISdMarFKCyWQCiqGGR72x9BVVib8EgPKkgELD6lgrLmXdFwoURWIqVtXnVpEyOsY9dXgbPT-jzjPAI210m4fF7l1zrYTTmF5l5BlZy_dGC-Xpvxa2iepW42X6QkdyNhT1Wq5cHpJbmNOPv6PL8nuAWUDDGPQfw14uGMQwYmlEQ1f-30PptqEEI2ZDIrcuTTc2tOOj5PKtSwUz3VAkKSQe5RnDkOYisb5jBxKR5uwMGSGVSaMTdfwBo0rmMQ)

```mermaid

flowchart
    classDef stable fill:#ggg,stroke:#EE2,stroke-width:4px;

    subgraph Ethereum
        direction TB
        wETH(wETH)
        Helix(Helix)
        ETH_USDC((USDC)):::stable
        ETH_USDT((USDT)):::stable
        DAI((DAI)):::stable
        Helix === |113,354| wETH
        DAI --- |20,441| ETH_USDC
        ETH_USDC --- |19,178| wETH
        DAI --- |19,692| wETH
        ETH_USDT --- |16,705| ETH_USDC
        Helix -..- |soon| ETH_USDC
    end

    subgraph Solana
        Sol(SOL)
        SOL_USDC((USDC)):::stable
        SOL_USDT((USDT)):::stable
    end

    subgraph BSC
        BNB(BNB)
        BUSDC((BUSD)):::stable
    end

    subgraph NEAR Protocol
        NEAR(NEAR)
        USN((USN)):::stable
    end

    subgraph Other Chain X
    end
```
