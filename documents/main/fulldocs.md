
# Resources

# Security & Audits

GHO has been implemented with security as priority. The system has been designed to be safe and secure, and we have spent all the necessary resources in order to ensure that the protocol matches the highest security standards.

Below are the links to all audit reports and formal verification for GHO

## Audit Round 1

| Auditor         | Date       | Report                                                                                             |
| --------------- | ---------- | -------------------------------------------------------------------------------------------------- |
| Sigma Prime     | 07-03-2023 | [SigmaPrime_GHO](https://github.com/aave/gho-core/blob/main/audits/07-03-2023_SigmaPrime.pdf)          |
| ABDK            | 01-03-2023 | [ABDK_GHO](https://github.com/aave/gho-core/blob/main/audits/01-03-2023_ABDK.pdf)                       |
| OpenZeppelin-v2 | 10-11-2022 | [OpenZeppelin_GHO_V2](https://github.com/aave/gho-core/blob/main/audits/10-11-2022_Openzeppelin-v2.pdf) |
| OpenZeppelin-v1 | 12-08-2022 | [OpenZeppelin_GHO_V1](https://github.com/aave/gho-core/blob/main/audits/12-08-2022_Openzeppelin-v1.pdf) |

## Glossary

| Term                   | Definition                                                                                                                                                                                                                                                                                     |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AAVE                   | The native asset of the Aave ecosystem, which constitutes the foundation of governance and safety for the Aave Protocol.                                                                                                                                                                       |
| Aave Protocol          | Decentralized protocol providing permissionless access to pooled money markets for cryptographic assets.                                                                                                                                                                                       |
| Arbitrage              | The concept of taking advantage of a difference in prices in multiple markets to make a profit.                                                                                                                                                                                                |
| Bucket                 | Defines the ability a Facilitator has to mint and burn GHO. Each Facilitator has its own Bucket that has a governance-controlled Capacity and a Level that is constantly being updated based on the Facilitator activity.                                                                      |
| Bucket Capacity        | Represents the upward limit of GHO that a specific Facilitator can generate.                                                                                                                                                                                                                   |
| Bucket Level           | The amount of GHO tokens generated per each Facilitator.                                                                                                                                                                                                                                       |
| Cooldown Period        | The time required prior to unstaking tokens, this is currently set to 864,000 seconds (10 days). Users can only withdraw their assets from the Security Module after the cooldown period ends and the unstake window is active.                                                                |
| Debt Token             | GHO, the discounted token.                                                                                                                                                                                                                                                                     |
| Discount Lock Period   | The minimum amount of time a user is entitled to a discounted interest rate without performing additional actions (expressed in seconds).                                                                                                                                                      |
| Discount Model         | Users that have staked AAVE tokens in the safety module (stkAAVE) are eligible for a discount on GHO. For each stkAAVE there will be a discount on the borrowing rate for 100 GHO. The discount model is subject to Aave Governance and can change.                                            |
| Discount Rate Strategy | Users that have staked AAVE tokens in the safety module (stkAAVE) are eligible for a discount on GHO. For each stkAAVE there will be a discount on the borrowing rate for 100 GHO.                                                                                                             |
| Discount Threshold     | The maximum amount of GHO that can be generated at discount through the borrow interaction within the Aave Protocol, per stkAAVE held.                                                                                                                                                         |
| Discount Token         | The token that grants discounts off of the the debt interest. Per the current configuration, only stkAAVE is eligible for the GHO borrowing discount.                                                                                                                                          |
| Facilitator            | A Facilitator can be a protocol or an entity within the crypto ecosystem, that has the ability to trustlessly mint (and burn) GHO tokens. They are assigned by the Aave Governance.                                                                                                            |
| Maximum Capacity       | The maximum capacity of GHO tokens that a Facilitator can mint                                                                                                                                                                                                                                 |
| Ray                    | For internal calculations and to reduce the impact of rounding errors, the concept of Ray Math is used. A Ray is a unit with 27 decimals of precision. All the rates are expressed in Ray.                                                                                                     |
| Reward Token           | The AAVE token is the reward token accrued when a user stakes in the Safety Module.                                                                                                                                                                                                            |
| Safety Incentives      | Represents the part of the periodic issuance of AAVE used to incentivize users to stake AAVE in the Safety Module (SM).                                                                                                                                                                        |
| Safety Module          | A smart contract-based risk mitigation tool that is leveraged in the event of a shortfall event. This component is in charge of shielding the protocol from insolvency, protecting the liquidity providers from risks resulting in loss of funds, such as liquidation and smart contract risk. |
| Shortfall Event        | Event in the Aave Protocol causing a state of deficit for the liquidity providers.                                                                                                                                                                                                             |
| Stablecoin             | Digital currencies pegged to reserve assets as a stabilization mechanism to prevent fluctuations in value.                                                                                                                                                                                     |
| Staked Token           | The AAVE token is staked in the Safety Module, stkAAVE.                                                                                                                                                                                                                                        |
| stkAAVE                | Represents a tokenized share of the Safety Module. When a user stakes AAVE in the Safety Module, the user receives an                                                                                                                                                                          |

----
docs/resources/SDK.md

----
docs/concepts/why-gho.md
---
sidebar_position: 1
---

# Why GHO?

Stablecoins play an important role in the DeFi ecosystem, offering a fast, efficient, and borderless way to transfer stable value. With many alternatives already in circulation, why develop a stablecoin?

### Market Demand

Based on the current state of the market, there is still limited adoption of decentralized stablecoins and room for growth.

### The Aave Protocol Is Well Positioned

The Aave Protocol already has the infrastructure to support many of the features needed to implement a stablecoin and will be the first Facilitator (see below) that can trustlessly mint and burn GHO tokens. At launch, if the community approves, there will be two [Facilitators](./how-gho-works/gho-facilitators.md) for GHO (the [Aave Protocol](./how-gho-works/gho-facilitators#aave-v3-ethereum-pool) and [FlashMinter](./how-gho-works/gho-facilitators#flashminter)); however, a framework with guidance on how to apply to the AaveDAO to become a Facilitator is open to community discussion on the [Aave Governance](https://governance.aave.com/) forum.

## Differentiating Factors

Significant demand exists for a stablecoin that is decentralized, over-collateralized, and configurable.

GHO, a stablecoin native to the Aave Protocol and controlled by Aave Governance, has the potential to make stablecoin borrowing on the Aave Protocol more competitive, provide more optionality for stablecoin users, and generate additional revenue for the Aave DAO by sending 100% of the interest payments accrued by minters of GHO directly to the [Aave DAO treasury](https://zapper.fi/daos/aave).

The Aave Protocol possesses key functionalities that are required to facilitate a decentralized stablecoin, such as supplying collateral and liquidations. As a result, if approved by the Aave community, the Aave Protocol will serve as one of the initial Facilitators for trustlessly minting and burning GHO tokens. As these functionalities already exist in the current Aave Protocol, GHO will fit natively into the existing Aave V3 Ethereum Pool as a new asset without requiring significant additional resources.

Below are factors that differentiate GHO from stablecoins available:

### Decentralized Stablecoins

Despite demand, there is a lack of decentralized stablecoins in the current DeFi landscape.

| Decentralized Stablecoins                                                                                                  | Centralized Stablecoins                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Enables a new level of transparency and censorship resistance, which reinforces the ethos of privacy and decentralization. | Require users to trust the issuer of the stablecoin. Centralized stablecoins can be blacklisted at any time and their backing may be opaque. |

Decentralized stablecoins, like GHO, provide censorship resistance, and most importantly, transparency for users.

GHO is decentralized and intentionally does not have one single concentrated point of control. GHO will be controlled by Aave Governance and the Aave Protocol’s community. With Aave Governance making all decisions relating to GHO, there is increased transparency with this asset in comparison to other stablecoins in the market. In addition, all [GHO code](https://github.com/aave/gho-core) is open source and has been [audited](../resources/resources.md#audit-round-1) extensively by security firms prior to launch. All protocol upgrades and updates to interest rates/risk parameters will be public and must be agreed upon in advance by Aave Governance prior to execution.

### Interest and Discount Rate Model

Discounts are available to borrowers staking AAVE in the Safety Module.

Please see the [Interest and Discount Rate Models](./how-gho-works/interest-rate-discount-model) page for more information.

### Multi-Collateral Positions

Traditionally in the DeFi ecosystem, users mint decentralized stablecoins via single asset-backed vaults. GHO is multi-collateralized, which means that users can mint GHO based on their entire set of supplied collateral assets across the Aave Protocol. As a result, GHO will be backed by various types of assets.

While there are key differences with respect to the implementation of GHO (please see the “[How GHO Works](./how-gho-works/how-gho-works.md)" page for a more detailed explanation), the process of interacting with the Aave Protocol and borrowing GHO is similar to that of other assets (i.e., a user will supply assets into the Aave Protocol and enable them to be used as collateral, and these assets can then be used to mint GHO, opening a multi-collateral backed borrowing position).

Using multiple different assets within the same borrowing position creates more flexibility for a user and allows for greater control over exposure to price fluctuations. This flexibility is beneficial for users in cases where they want to increase their health factor. Having multi-collateral positions means that a user would not have to balance multiple positions and health factors and would not have to swap between assets to fund a position.

### Interest-Earning Collateral

When a user supplies collateral to the Aave Protocol, other users will borrow the supplied assets. Interest will be earned on the supplied collateral, which effectively reduces the interest that a user is paying on their borrowed positions.

Therefore, the collateral used to mint GHO will actively earn interest.

### Trustless Minting

Trust is an essential component of a stablecoin. GHO introduces the concept of Facilitators. A Facilitator (e.g., a protocol or an entity) can trustlessly mint and burn GHO tokens.

Facilitators must be approved by the Aave DAO and can apply different strategies to their generation of GHO.

Please see the [Facilitators](./how-gho-works/gho-facilitators.md) page for more information.

## The Future of GHO

Stablecoins are tied to the wider adoption of the crypto ecosystem by making stablecoins the currency of web3.

### Aave Roadmap

Synergies with the Aave Protocol ecosystem, future products, and deployments make GHO critical for the Aave Protocol’s future roadmap.

### L2s

There is a large opportunity for GHO to have widespread usage on L2s given their lower fees. This could be enabled through bridging, or additional minting.

### Additional Facilitators

If approved by the community, the Aave V3 Ethereum Pool and FlashMinter will be the first two Facilitators enabled to mint GHO. In the future, Aave Governance may vote to add additional Facilitators. Once a new Facilitator is approved, it will have the ability to mint GHO.

### DeFi Ecosystem

The usage of stablecoins is likely to grow as more people are onboarded into crypto and the number of blockchain transactions increases.

## How does developing GHO benefit users?

Based on how GHO is designed, it will provide more utility to Aave Protocol users and the Aave DAO.

Aave Governance makes all decisions pertaining to GHO. This provides transparency and allows the community to manage GHO, Facilitators, and interest rates.

Users of the Aave Protocol can borrow GHO, based on the collateral supplied to the protocol. This means users have access to a decentralized multi-collateral backed stablecoin, with competitive interest rates, whilst earning interest on their collateral supplied.

Users who participate in staking their AAVE tokens in the Safety Module will benefit by having access to a discount on the borrow rate of GHO. Therefore, holders of AAVE are incentivized to stake it, while helping to secure the Aave Protocol as AAVE flows into the protocol’s Safety Module.

----
docs/concepts/intro.md
---
id: overview
title: What Is GHO?
sidebar_position: 1
---

### **GHO is a decentralized multi-collateral stablecoin that is fully backed, transparent and native to the Aave Protocol.**

GHO (pronounced "go") is a decentralized multi-collateral stablecoin that is initially only minted from assets supplied to the Aave Protocol. GHO’s value is programmatically aligned to the U.S. Dollar, which will be maintained through market efficiency.

As a decentralized stablecoin on the Ethereum Mainnet, GHO will be minted by users. As with all borrowing on the Aave Protocol, a user must supply collateral (at a specific collateral ratio) to be able to mint GHO. Correspondingly, when a user repays a borrow position (or is liquidated), the GHO is returned to the Aave pool and burned. All the interest payments accrued by minters of GHO will go directly to the [Aave DAO treasury](https://zapper.fi/daos/aave), in contrast to the standard reserve factor collected when users borrow other assets, and the principal is burned.

Significant demand exists for a stablecoin that is truly decentralized, over-collateralized, and configurable. Recent events have demonstrated the use case for decentralized stablecoins as a means of maintaining a stable value during periods of market volatility. GHO, a stablecoin controlled by Aave Governance, has the potential to become an integral part of the continued growth of the DeFi ecosystem with community support.

Explore the GHO documentation to understand how it works and why the development of GHO is essential for the broader ecosystem. The [Technical Paper](https://github.com/aave/gho-core/blob/main/techpaper/GHO_Technical_Paper.pdf) and Smart Contracts pages will provide guidance on how to integrate GHO.

----
docs/concepts/_category_.json
{
  "label": "Concepts",
    "position": 2
}
----
docs/concepts/faq.md
# GHO FAQ

## What is GHO?

GHO is a decentralized multi-collateral stablecoin that is fully backed, transparent and native to the Aave Protocol.

## How is the value of GHO kept stable?

GHO will be kept stable through market efficiencies. It is envisioned that if GHO were to be valued > $1, the market would [arbitrage](../concepts/fundamental-concepts/arbitrage.md) the value back to $1 as it would be profitable to swap GHO for other stablecoins. If GHO were to be valued < $1, then it would be profitable to pay back debt, and will result in GHO total supply decreasing as debt is repaid will help the peg to be restored.

## How to mint GHO?

Borrowers and suppliers can mint GHO using assets they have supplied into V3 as collateral on Ethereum markets, while continuing to earn interests on their underlying assets.

## How to borrow GHO

The GHO pool will function differently from existing assets but to borrow it will work similarly as other available assets on the different markets in the protocol. 

1. Supply Collateral
2. Borrow GHO
3. Repay GHO and Accrued Interest (real-time)
4. Repaid interest will be redirected to the DAO, rather than an asset supplier, contributing to the DAO treasury

The video below shows how to borrow GHO using the Aave Protocol interface.

<video controls width="100%" autoPlay>
  <source src="https://gho.infura-ipfs.io/ipfs/QmVFGEyoMTaoYnMCL9oDEg2zwaxK9G2T2vqEHUN7tu8Qtk"/>
</video>

## How is GHO different from the other assets listed on the Aave markets?

Unlike many stablecoins, the oracle price for GHO will be fixed. Decentralized stablecoins such as GHO are transparent and cannot be changed. Interest rates are defined by the Aave DAO and repaid interest is redirected to the DAO instead of the asset suppliers. Discounts are available to borrowers staking AAVE in the Safety Module.

## Which assets can be used as collateral to borrow GHO?

Assets that are available in the Aave Protocol can be used to back GHO. Initially, the Ethereum V3 pool will be the first facilitator to launch because of V3’s extensive risk-mitigation features, including e-mode, isolation mode, and supply caps.

## Who manages the GHO supply?

The Aave DAO will manage the supply of GHO, the interest rates and determine risk parameters.

## What is a Facilitator and what does it mean for GHO?

GHO introduces the concept of [Facilitators](../concepts/how-gho-works/gho-facilitators.md). A Facilitator (e.g., a protocol, an entity, etc.) has the ability to trustlessly mint (and burn) GHO tokens. To be added as a Facilitator they would have to be approved by Aave Governance. Various Facilitators will be able to apply different strategies to their generation of GHO. 

## Can you explain more about the discount model for GHO?

Users that have staked AAVE tokens in the Safety Module (stkAave) are eligible for a discount on GHO.

For each stkAave there will be a discount on the borrowing rate for 100 GHO. The discount model is interchangeable and can be redesigned and replaced if needed by The Aave DAO. The first decision regarding the GHO interest and discount rates can be seen [here](../concepts/fundamental-concepts/gho-discount-strategy.md).

## Is only stkAAVE used for discount or is aBPT eligible? If not, why?

Currently only stkAAVE.

## Can GHO be flashloaned?

GHO can be [FlashMinted](../concepts/fundamental-concepts/flashmint.md). FlashMinting provides the same functionality and follows the current Flash Loan standard (ERC3156) as in the Aave Protocol.

----
docs/concepts/fundamental-concepts/borrow-gho.md
---
sidebar_position: 2
---

# Borrow GHO

Borrowing GHO is actually minting GHO ‘under the hood’. GHO will be borrowed by users (or borrowers) via [Facilitators](../how-gho-works/gho-facilitators.md). As with all borrowing on the Aave Protocol, a user must supply collateral (at a specific collateral ratio) to mint GHO.

## Borrowing on the Aave Interface

The video below shows how to borrow GHO using the Aave Protocol interface. This gives an overview of the process and steps involved before looking at how to mint GHO from a smart contract level.

<video controls width="100%" autoPlay>
  <source src="https://gho.infura-ipfs.io/ipfs/QmVFGEyoMTaoYnMCL9oDEg2zwaxK9G2T2vqEHUN7tu8Qtk"/>
</video>

## Minting GHO

GHO is created (‘[minted](../../developer-docs/overview#minting)’) by Facilitators. GHO is collateralized by the supply of crypto assets in excess of the value of GHO to be minted. This over-collateralization is intended as a stabilization mechanism to reduce the impact of any price fluctuations on the value of the underlying collateral during periods of volatility.

![Borrow Diagram](../../assets/GHO_borrow_process.png#gh-dark-mode-only)
![Borrow Diagram](../../assets/GHO_borrow_process_dark.png#gh-light-mode-only)

When borrowing GHO, based upon standard collateralization requirements built into the smart contracts, new GHO and GHO Debt Tokens are automatically generated and transferred to the user.

During a borrow transaction, the Bucket level for the Facilitator is updated to reflect the new amount of GHO minted.

The borrow action fails if the amount requested exceeds the Bucket capacity assigned to the Facilitator.

### Example Scenario

- The user supplies 1 ETH as collateral to the Aave Protocol
- The user receives 1aWETH in their wallet in return
- The user borrows (mints) 10 GHO
  - The GHO borrow rate can be discounted by holding stkAAVE
- They receive 10 debt tokens
- The debt becomes 10.00000008 variableDebtEthGHO because of interest after a short period of time.

It is important to take note of health factors, as with any other assets. Changes in the collateral price will impact the user's health factor, and if the health factor falls below 1, their collateral can be liquidated.

----
docs/concepts/fundamental-concepts/supply-gho.md
---
sidebar_position: 1
---

# Supply GHO

Given the nature of GHO and the way it interacts with Aave, GHO cannot be supplied to the Aave V3 Ethereum Pool where it is minted.

![Supply Diagram](../../assets/Supply_dark.png#gh-dark-mode-only)
![Supply Diagram](../../assets/Supply.png#gh-light-mode-only)

## Benefits

As GHO is not supplied, there are benefits to the way GHO works in comparison to other assets.

### Flexibility

No one has to have supplied GHO for a user to borrow it. Instead, the protocol calls the GHO contract and mints that GHO on demand.

### Decentralization

GHO smart contracts do not follow usual supply and demand dynamics, as the supply side does not exist. Therefore, interest rates are not determined by utilization rates as they are with other stablecoins. For GHO, interest rates are determined by the Aave Governance.

As GHO is decentralized, GHO intentionally does not have one single concentrated point of control.

### Competitive Interest Rates

As GHO is not supplied, there are no suppliers to pay. The interest accrued on positions can be paid straight to the DAO.

----
docs/concepts/fundamental-concepts/flashmint.md
---
sidebar_position: 5
---

# FlashMint

FlashMinting is an important transaction for GHO as it helps to facilitate arbitrage and the ability to liquidate users.

:::info
Developers see [here](../../developer-docs/developer-docs-overview.md#flashmint)
:::

## Flashloan vs FlashMinting

In the current Aave Pool, if an asset is supplied, a user is able to perform a Flash Loan transaction with this asset. As GHO is not supplied, performing a Flash Loan is not possible. There is no problem with this, however, the GHO reserve is configured to disable native flashloans.

Therefore, FlashMinting has been introduced. FlashMinting provides the same functionality and follows the current [Flash Loan](https://docs.aave.com/developers/guides/flash-loans) standard (ERC3156) as in the Aave Protocol. Allowing users to access the liquidity of the FlashMinter Facilitator for one transaction, as long as the amount taken plus the fee is returned or (if allowed) debt position is opened by the end of the transaction.

The [FlashMinter Facilitator](../how-gho-works/gho-facilitators#flashminter) is an entity that enables FlashMinting. The FlashMinter has a GHO limit to mint and will be proposed as an initial Facilitator to the Aave DAO.

## Execution Flow

For developers, a helpful mental model to consider when developing a solution is as follows:

1. Your contract calls the FlashMinter Facilitator, requesting to FlashMint a certain amount of GHO using [`flashLoan()`](../../developer-docs/flashmint-facilitator/GhoFlashMinter#flashloan).
2. If the requested amount is lower or equal to the Facilitator's capacity, the FlashMinter Facilitator mints and transfers the GHO amount to your contract, then calls `onFlashLoan()` on receiver contract.
3. Your contract, now holding the FlashMinted amount, executes any arbitrary operation in its code.
   - You approve the FlashMinter Facilitator for FlashMinted amount + fee. If you are an authorized flashborrower by the Aave DAO, your fee is 0.
   - You return the keccak hash of `ERC3156FlashBorrower.onFlashLoan` so the FlashMinter Facilitator ensures the receiver is ERC3156 complaint.
   - If any of these conditions are not met or the amount owing is not available (due to lack of balance or approval), then the transaction is reverted.
4. All of the above happens in 1 transaction (hence in a single block).

## Step by step

1. **Setting Up**

Your contract that receives the FlashMinted amount of GHO must conform to the ERC3156 standard. The [`IERC3156FlashBorrower.sol`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/interfaces/IERC3156FlashBorrower.sol) interface defines the relevant `onFlashLoan()` function that needs to be overridden by your arbitrary code.

Also note that since the owed GHO amount will be pulled from your contract, your contract must give allowance to the FlashMinter Facilitator to pull those funds to pay back the FlashMinted amount + fee.

2. **Calling `flashLoan()`**

To call the flash loan method of the FlashMinter Faciltiator, we need to pass in the relevant parameter.
There are 3 ways you can do this:

**From an EOA ('normal' Ethereum account)**
To use an EOA, send a transaction to the relevant Pool calling the flashLoan() function. See FlashMinter api docs for parameter details, ensuring you use your contract address from step 1 for the receiver.

**From a different contract**
Similar to sending a transaction from an EOA as above, ensure the receiver is your contract address from step 1.

**From the same contract**
If you want to use the same contract as in step 1, use `address(this)` for the receiver parameter in the flash loan method.

3. **Completing the flash loan**

Once you have performed your logic with the FlashMinted asset (in your `onFlashLoan()` function), you will need to pay back the FlashMinted amount plus the fee.

**Paying back the FlashMinted asset**
Ensure your contract has the relevant amount + fee to payback the borrowed asset. You can calculate this by taking the sum of the amount and fee values passed into the `onFlashLoan()` function.
You do not need to transfer the owed amount back to the FlashMinter Facilitator. The funds will be automatically pulled at the conclusion of your operation.

**Returning the correct value in `onFlashLoan()`**
The FlashMinter Facilitator checks the returned value of `onFlashLoan()` to validate it is ERC3156 complaint. The correct value to return is the keccak hash of `ERC3156FlashBorrower.onFlashLoan` string.

----
docs/concepts/fundamental-concepts/_category_.json
{
  "label": "GHO Fundamentals",
  "position": 3,
  "link": {
    "type": "generated-index"
  }
}
----
docs/concepts/fundamental-concepts/gho-discount-strategy.md
---
sidebar_position: 4
---

# Discount Rate Strategy

Given the nature of the asset, this integration allows for innovative features that provide greater utility for Governance and community participants. The implementation of GHO includes a Discount Strategy mechanism. The initial discount strategy allows Safety Module participants (users who have [staked AAVE](https://docs.aave.com/faq/#aave-aave-token) and now hold stkAAVE) to access a discount on the GHO borrow rate. The strategy sets a certain amount of GHO at a discount per stkAAVE , and a discount on the interest rates that can vary from 0% (no discount) to 100% (full discount). Only stkAAVE is eligible for the GHO borrowing discount.

The configuration of the discount rate is controlled by [Aave Governance](https://governance.aave.com/). Aave Governance has the right to determine the discount model parameters and eventually propose changes to the current implementation.

By contributing to the Safety Module, users are taking a risk that they in the case of bad debt arising in the Aave protocol. To incentivize users to participate in staking, and reward them for taking this risk, users staking AAVE can receive a discount on their interest rate.

## Discount Rate Updates

The discount model is designed to be updated easily, therefore if Governance determines a different strategy is required, it can be implemented efficiently. Governance may decide to change the strategy in situations when too many users have a very good discount rate.

The discount rate is available to the user for a certain period of time and is subject to change whenever a user triggers a discount update or is rebalanced.

When a user receives a discount, it is assigned to them for a certain period, for example, 6 months. After the aforementioned, if Aave Governance has set a new discount strategy, and the user receives another discount rate, it may not be the same, it will have changed to the rate updated by Governance.

This may also happen if a user triggers a discount update, such as, borrowing and repaying GHO, and updating their stkAAVE balance.

## Initial Implementation

The initial implementation of the discount model on borrow rates defines:

- A maximum amount of GHO that can be generated at a discounted rate through borrowing within the Aave Protocol, per stkAAVE held.
- A discount on the borrow rate that the user will receive per discounted GHO.

Given the discount model, the final borrow rate a user will receive is defined as follows:

$$
\small R_{GHO_u} = \begin{dcases}   R_{GHO}                                                                   &\text{if } B_{stkAAVE}(u) = 0 \cr   R_{GHO} - R_{GHO} * R_d                                                   &\text{if } B_{stkAAVE} > 0 \land P(u) \leq B_{stkAAVE} * T \cr   \frac{R_{GHO} * P_{nd}(u) + (R_{GHO} - R_{GHO} * R_d) * P_d(u)} {P(u)}      &\text{if } B_{stkAAVE} > 0 \land P(u) \gt B_{stkAAVE} * T\end{dcases}
$$

Where:

| Variable         | Description                                                                                                                                          |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| $u$              | The user                                                                                                                                             |
| $B_{stkAAVE}(u)$ | The stkAAVE balance of the user $u$                                                                                                                  |
| $R_{GHO_u}$      | The current, governance controlled borrow rate for GHO (without any discount applied), $0 ≤ R_{GHO} ≤ 1$                                             |
| $T$              | The maximum amount of GHO that can be generated at discount through the Borrow interaction within the Aave Protocol, per stkAAVE held (per user $u$) |
| $R_d$            | The global discount rate, the discount on the borrow rate that the user will receive per discounted GHO tokens, $0 ≤ R_d ≤ 1$                        |
| $P(u)$           | The current principal borrowed by the user $u$, in GHO tokens                                                                                        |
| $P_d(u)$         | The part of the principal at a discount (when $B_{stkAAVE} > 0$), $P_d(u) = B_{stkAAVE(u)} * T$                                                      |
| $P_{nd}(u)$      | The part of the principal that exceeds the discount (when $B_{stkAAVE} > 0$), $P_{nd}(u) = P(u) − P_d(u)$                                            |

:::caution

The forumla is an estimate of the final interest rate the user will receive.

:::

The following examples help to explain the above equation:

### Example 1

The current interest rate is 2%, and the user ($u$) has not staked any AAVE in the Safety Module.

Given:

- $R_{GHO} = 0.02$
  - The borrow rate
- $B_{stkAAVE}(u) = 0$
  - The user does not have stkAAVE

$B_{stkAAVE}(u) = 0$

Therefore:

$\begin{aligned}
R_{GHO_u} &= R_{GHO} \\
    &= 0.02
\end{aligned}$

As the user has not staked AAVE in the Safety Module, they are not eligible for a discount on the borrow rate. They can borrow GHO with the current, governance-controlled borrow rate, in this example, 2%.

### Example 2

The current interest rate is 3%. Per stkAAVE, a user can receive a 50% discount on interest, for 100 GHO tokens. The user stakes 1 AAVE and borrows 100 GHO.

Given:

- $R_{GHO} = 0.03$
  - The borrow rate
- $T = 100$
  - The maximum amount of GHO available for the user to borrow at a discount
- $R_d = 0.5$
  - The discount available on the borrow rate
- $P(u) = 100$
  - The amount of GHO borrowed by the user
  - This is the maximum amount the user can borrow at a discount - $T$
- $B_{stkAAVE}(u) = 1$
- $P_d(u) = T * B_{stkAAVE}(u) = 100 * 1 = 100$
  - The amount of GHO the user has borrowed at a discount
- $P_{nd}(u) = P(u) − P_d(u) = 100 − 100 = 0$
  - The amount of GHO borrowed that exceeds the discount

$B_{stkAAVE} > 0 ∧ P(u) ≤ B_{stkAAVE} * T$

Therefore:

$\begin{aligned}
R_{GHO_u} &= R_{GHO} - R_{GHO} * R_d \\
       &= 0.03 - 0.03 * 0.5 \\
       &= 0.015
\end{aligned}$

The user has staked AAVE in the Safety Module, and the amount of GHO they have borrowed has not exceeded the maximum amount of GHO to borrow at a discount. Their interest rate is 50% of 3%. They can borrow GHO with a discounted borrow rate, in this example, 1.5%.

### Example 3

The current interest rate is 3%. Per stkAAVE, a user can receive a 50% discount on interest, for 100 GHO tokens. The user stakes 1 AAVE and borrows 200 GHO (compared to 100 GHO in Example 2).

Given:

- $R_{GHO} = 0.03$
  - The borrow rate
- $T = 100$
  - The maximum amount of GHO available for the user to borrow at a discount
- $R_d = 0.5$
  - The discount available on the borrow rate
- $P(u) = 200$
  - The amount of GHO borrowed by the user
  - This exceeds the maximum amount the user can borrow at a discount - $T$
- $B_{stkAAVE}(u) = 1*$
- $P_d(u) = T * B_{stkAAVE}(u) = 100 * 1 = 100$
  - The amount of GHO the user has borrowed at a discount
- $P_{nd}(u) = P(u) − P_d(u) = 200 − 100 = 100$
  - The amount of GHO borrowed that exceeds the discount

$B_{stkAAVE} > 0 ∧ P(u) > B{stkAAVE} * T$

Therefore:
$\begin{aligned}
R_{GHO_u} &= \frac{R_{GHO} * P_{nd}(u) + (R_{GHO} - R_{GHO} * R_d) * P_d(u)} {P(u)} \\
       &= \frac{0.03 * 100 + (0.03 - 0.03 * 0.5) * 100} {200} \\
       &= 0.0225
\end{aligned}$

The user has staked AAVE in the Safety Module, and the amount of GHO they have borrowed has exceeded the maximum amount of GHO to borrow at a discount. Therefore, they only get a discount on part of the GHO borrowed. 100 of the GHO borrowed will be at a 1.5% discount rate, and their effective interest rate will be 2.25%.

----
docs/concepts/fundamental-concepts/arbitrage.md
---
sidebar_position: 6
---

# Arbitrage

Users can always borrow, repay and liquidate GHO at 1 US Dollar. By fixing the price of GHO to $1, immediate arbitrage opportunities are created. Arbitrage is a stabilizing factor for GHO and is necessary to help maintain the peg at 1 USD.

The example situations below help to understand GHO arbitrage opportunities.

## GHO Price is Above Peg

When the market price of GHO is above $1, there is the incentive to generate new GHO and sell on the market, repaying once the price has lowered enough to be profitable.

If the GHO price is above the peg ($1) in the market, users can mint 1 GHO for $1 worth of debt, and sell their GHO for more than $1. The minter can later repay their debt at $1 while keeping the difference of what they sold GHO at. This increases the supply of GHO while decreasing the price of GHO.

For example:

- The price of GHO in the protocol is $1

- The price of GHO on the market is above peg, at $1.05

- A user mints 1 GHO from the Aave Protocol for $1

- This user can then sell their GHO on the market for $1.05

- This increases the supply of GHO on the market

- As there is more GHO available on the market, the price of GHO should decrease (due to supply and demand) to $1

- The user can then buy GHO on the market at $1

- The user can repay their $1 worth of debt to the Aave Protocol

- The user keeps the difference of what they sold their GHO at, $0.05 profit

## GHO Price is Below Peg

When the market price of GHO is below $1, there is an incentive for borrowers to purchase GHO at a discounted price and repay/liquidate, earning on the difference.

If the GHO price is below peg ($1) in the market, minters can acquire 1 GHO on the market for less than $1, and pay off $1 worth of debt. This action shrinks the supply of GHO while increasing the asset price.

For example:

- The price of GHO in the protocol is $1

- The price of GHO on the market is below peg, at $0.95

- A user who already has a borrow position can acquire GHO from the market for $0.95

- The user can repay their $1 worth of GHO debt for less than $1 (with the GHO they acquired for $0.95)

This should increase the demand for GHO, and therefore decrease the supply of GHO on the market, while increasing the price.

## FlashMinting

[FlashMinting](../fundamental-concepts/flashmint.md) provides the same functionality as the current flashloan standard and can be used in the same way flashloans are regularly used for arbitrage within the Aave Protocol. Therefore, FlashMinting can be used for arbitrage between assets, without needing to have the principal amount (borrow position) to execute the arbitrage.

----
docs/concepts/fundamental-concepts/repay-liquidate-gho.md
---
sidebar_position: 3
---

# Repay and Liquidate GHO

When a user repays their GHO (or is liquidated), that user’s GHO is burned by the [Facilitator](../how-gho-works/gho-facilitators.md).

## Repaying on the Aave Interface

The video below shows how to repay GHO using the Aave Protocol interface. This gives an overview of the process and steps involved before looking at how to repay GHO from a smart contract level.

<video controls width="100%" autoPlay>
  <source src="https://gho.infura-ipfs.io/ipfs/QmPyAUsHBv385WgBaWB2rvrAyzAzGzuqRPzsnPUj5Jtsix"/>
</video>

## Repaying or Liquidating GHO

When [repaying](../../developer-docs/overview#repay) (or [liquidating](../../developer-docs/overview#liquidation)) GHO, first there are automatic smart contract-based collateralization checks. GHO is then returned to the pool from the user (or liquidator) and burned.

Normal assets direct the majority of interest earned to users who have supplied the corresponding asset, and a small portion is directed to the DAO. In this instance, since there are no suppliers to pay, the interest (accrued by minters of GHO) that is repaid is automatically transferred to the Aave DAO treasury. While the original amount of GHO is burned, and the Bucket level for the Facilitator is decreased.

![Repay Diagram](../../assets/Repay_and_liquidate_dark.png#gh-dark-mode-only)
![Repay Diagram](../../assets/Repay_and_liquidate.png#gh-light-mode-only)

### Example Scenario

- The user has 10 debt tokens
- The user purchases 90 GHO tokens on the market, ending up with 100 GHO tokens.
- The debt becomes 10.00000008 variableDebtEthGHO because of interest after a short period of time.
- The user has to approve for the Aave Protocol to pull funds from them to repay
- The user then repays their GHO debt position (using the repayWithPermit() function)
  - The 10.00000008 GHO gets repaid to the Aave Protocol and 10.00000008 variable debt tokens are burned.
  - The principal part, 10 GHO, gets burned by the Aave Facilitator and the interest earned, 0.00000008 GHO, is transferred to the GHO treasury.

## Liquidations

Users can be liquidated on their GHO borrow positions, the same as any other asset in the Aave Protocol.

When a liquidation occurs, liquidators repay up to 50% of the outstanding borrowed amount on behalf of the borrower. In return, they can buy the collateral at a discount and keep the difference (liquidation penalty) as a bonus.

It is important to be mindful of price fluctuations due to market conditions, as changes in the collateral price will impact the health factor and may lead to liquidations. If the health factor goes below 1, the liquidation of collateral might be triggered. To avoid liquidations more collateral can be supplied or borrow positions can be repaid.

### FlashMint

[FlashMinting](flashmint.md) provides the same functionality as the current flashloan standard. Therefore, FlashMinting can be used to liquidate borrow positions, the same way flashloans are regularly used to liquidate user positions within the Aave Protocol. Additionally, users approved by the Aave DAO as “_FlashBorrowers_” have the ability to execute flash mints free of charge. This works in the same way as the “flashLoan” function of the Aave V3 protocol.

For more information, please read the liquidation pages in the [FAQs](https://docs.aave.com/faq/liquidations) and [V3 Developer Docs](https://docs.aave.com/developers/guides/liquidations).

----
docs/concepts/how-gho-works/gho-governance.md
---
sidebar_position: 3
---

# Governance

The Aave Protocol is a fully decentralized, community-governed protocol, managed by AAVE (and stkAAVE) token holders. Token holders collectively discuss, propose, and vote on upgrades to the Aave Protocol through [Aave Governance](https://governance.aave.com/). AAVE and stkAAVE token holders (Ethereum network only) can either vote on new proposals or delegate their voting power to an address of choice.

As GHO is decentralized, it does not have a single concentrated point of control. Instead, GHO is controlled by Aave Governance. The Aave Companies do not have any control over GHO.

## Governance Resources

The Aave Companies [introduced GHO](https://governance.aave.com/t/introducing-gho/8730) to the Aave DAO on July 7, 2022.

Following a period of discussion, the community voted to greenlight GHO via [Snapshot](https://snapshot.org/#/aave.eth/proposal/0xb17b3294dcb08316cb623c717add7f82df54948d558992f886be59d0958e9b24).

The first [GHO Development Update](https://governance.aave.com/t/gho-development-update/10267) was published on October 14, 2022.

The second [GHO Development Update (Testnet Release)](https://governance.aave.com/t/gho-development-update-testnet-release/11631) was published on February 9, 2023.

## Governance Role

Aave Governance has the right to determine GHO Facilitators and parameters and to propose changes to the current implementation. Frameworks and processes for Facilitators, caps, and rates are open to community discussion.

### Facilitators

Aave Governance has control over the entities that are added and removed as [Facilitators](./gho-facilitators.md). Every Facilitator will have to be carefully audited and reviewed by Aave Governance before receiving mint permissions. Each Facilitator will have a governance-defined limit on how much GHO it can mint.

By carefully approving each Facilitator, Aave Governance can manage exposure to different [strategies](./gho-facilitators.md#facilitator-strategies). Aave Governance may want to attract varied Facilitators in several different ways. This could also include strategies for non-Aave users. If non-Aave Protocol Facilitators are approved by Aave Governance, the possibilities and use cases could be endless (e.g., use within payment applications and e-commerce solutions, purchases of GHO on decentralized exchanges, and use as a store of value during market volatility).

### Interest and Discount Rates

Aave Governance can set the interest rates of GHO, the discount threshold (i.e., the maximum amount of GHO that can be generated at a discount), and the discount rate to stimulate the generation (i.e., expansion) or destruction (i.e., contraction) of GHO.

Aave Governance can periodically set the interest rates of GHO based on supply and demand models. Both the interest rate and the discount rate are configurable by Aave Governance.

For more information, please see the [Interest and Discount Rates](interest-rate-discount-model.md) page.

## Aave DAO Impact

With the GHO model, 100% of interest paid on borrowed GHO goes to the Aave DAO. Depending on the demand for GHO, this could result in substantial revenue for the Aave DAO. Alongside this, the [FlashMint](../fundamental-concepts/flashmint.md) module generates revenue through the fees from the transaction. As mentioned above, there may be various strategies implemented for future Facilitators. It is possible that future Facilitators may also redirect some revenue to the DAO.

----
docs/concepts/how-gho-works/gho-facilitators.md
# Facilitators

## What is a Facilitator?

GHO introduces the concept of Facilitators. A Facilitator can trustlessly mint and burn GHO tokens through various strategies. These strategies can be enacted by different entities that may employ varying strategies for integrating GHO (each entity, a Facilitator). The Aave DAO assigns each Facilitator a Bucket with a specified Capacity, which is the upward limit of GHO that a specific Facilitator can mint. This limit is defined and can be changed by the Aave DAO.

![Facilitator Diagram](../../assets/facilitator_dark.png#gh-dark-mode-only)
![Facilitator Diagram](../../assets/facilitator.png#gh-light-mode-only)

## Current Facilitators

It has been proposed to the Aave community that the Aave V3 Ethereum Pool and FlashMinter Facilitator will be the first Facilitators of GHO.

### Aave V3 Ethereum Pool

The Aave V3 Ethereum Pool has been proposed to the Aave DAO to serve as one of the initial Facilitators on the Ethereum Mainnet due to the risk-reducing features of this version of the protocol, including [efficiency mode](https://docs.aave.com/developers/whats-new/efficiency-mode-emode) (“eMode”), [isolation mode](https://docs.aave.com/developers/whats-new/isolation-mode), [siloed borrowing](https://docs.aave.com/developers/whats-new/siloed-borrowing), and [caps](https://docs.aave.com/developers/whats-new/supply-borrow-caps). In addition, it will assist with bootstrapping the GHO supply in a decentralized and permissionless fashion.

The [Aave Protocol](https://aave.com/) is a liquidity protocol available on Ethereum and various other L1 and L2 networks. Aave allows users to supply a range of assets and borrow against them while simultaneously earning yield, as well as participating in liquidations. The Aave Protocol operates on an overcollateralized model. Accordingly, GHO will be overcollateralized as well.

### FlashMinter

The FlashMinter Facilitator is an entity that enables [FlashMinting](../fundamental-concepts/flashmint.md). FlashMinting is especially important for GHO as it will help to facilitate arbitrage, provide instant liquidity, and have the ability to liquidate users.

As FlashMinting provides the same functionality as the current [flashloan](https://docs.aave.com/developers/guides/flash-loans) standard, it works very much the same (e.g. everything must be returned and there will be a fee).

### Become a Facilitator

Each Facilitator must be approved by [Aave Governance](https://governance.aave.com/). Aave Governance will be able to determine and assign a Facilitator a specific Bucket capacity to bootstrap GHO liquidity and the GHO market.

Frameworks on how to apply to become a Facilitator will be open to community discussion.

## Facilitator Strategies

GHO will be minted through various strategies. Eventually, Facilitators will be able to apply different strategies to their generation of GHO. This will allow Aave Governance to manage its exposure to different strategies across the ecosystem, and some strategies may help GHO maintain its peg.

As it will be up to Facilitators to decide their minting strategies, we expect to see exciting creativity in this area. For example, the Aave V3 Pool, one of the proposed initial Facilitators of GHO, operates on an overcollateralized model. As a result, GHO will be overcollateralized.

Aave Governance may attract varied Facilitators in different ways. If new and additional Facilitators are approved by Aave Governance, the possibilities are endless.

## Facilitator Technical Fundamentals

A Facilitator ($F$) can trustlessly generate and burn GHO tokens. Each Facilitator is assigned a Bucket ($B$) with a specified Capacity ($C$). The Capacity ($C$) represents the upward limit of GHO that a specific Facilitator can generate. The amount of GHO tokens generated per each Facilitator is called Level ($L$). Fundamentally, all Facilitators must adhere to the following equation:

Given a set of Facilitators $F_0, F_1, ...F_{N − 1}$ each of which is associated with a certain Bucket with capacity ($CB_t$) and a current Bucket level at a given time ($LB_t$). The Available Supply ($AS_{GHO_t}$), is the maximum amount of GHO available to be minted through all the Facilitators at a given time ($t$), defined as follows:

$$
AS_{GHO_t} = \sum_{n=0}^{N-1} max(0, CB(n)_{t} - LB(n)_{t})
$$

:::info

It is important to note the exception to this preliminary equation. As the Bucket Capacity can be changed by the Aave DAO, there is the possibility that a Facilitator could result in having more GHO minted than its initial Capacity. This may occur if the Bucket’s Capacity has been lowered by the Aave DAO.

:::

Facilitators can be different in technical nature. As stablecoins can differ depending on the stabilization mechanisms they employ, with GHO, the idea is to employ multiple stabilization mechanisms, in a controlled fashion via the Aave DAO by properly balancing each Bucket capacity to not compromise overall system collateralization and stability.

----
docs/concepts/how-gho-works/how-gho-works.md
# How GHO Works

GHO is a flexible, decentralized multi-collateral stablecoin on the Ethereum Mainnet. It is available in the form of an ERC20 token that is designed to maintain a stable rate, pegged to the U.S. dollar, despite market volatility. GHO natively fits into the existing Aave Protocol as a new asset, meaning that interacting with the protocol to borrow GHO will be similar to interacting with other assets in the Aave Pool:

![GHO_Architecture Diagram](../../assets/GHO_Architecture_dark.png#gh-dark-mode-only)
![GHO_Architecture Diagram](../../assets/GHO_Architecture.png#gh-light-mode-only)

**Supply Collateral –> Borrow GHO –> Repay GHO Debt**

GHO is created (“minted”) or repaid (“burned”) by Facilitators. GHO is minted upon the supply of assets more than the value of GHO to be minted. GHO is designed to accrue interest when it is borrowed, and this interest rate is determined by [Aave Governance](https://governance.aave.com/).

The following pages and technical paper describe the fundamental characteristics and smart contract design of GHO.

### GHO Implementation

While interacting with GHO is similar to interacting with other assets within the Aave Protocol, the [implementation](gho-implementation.md) of and user interaction with GHO as an asset in the Aave pool is quite different. The way that GHO is configured has differences that help it to maintain price stability.

### Interest and Discount Rates

The interest rate is the cornerstone of GHO stability, and, as in all decentralized protocols, it is built into the code. GHO smart contracts do not follow the usual supply and demand dynamics that can often impact interest rates. Both the [interest rate and the discount rate](interest-rate-discount-model.md) are configurable by Aave Governance. The implementation of GHO includes a Discount Strategy mechanism, which allows for Safety Module participants (i.e., stkAAVE holders) to access a discount on the GHO borrow rate.

### Facilitators

GHO introduces the concept of [Facilitators](gho-facilitators.md). A Facilitator can trustlessly mint and burn GHO tokens through various strategies. These strategies can be enacted by different entities that may employ varying strategies for integrating GHO (each entity, a Facilitator). The Aave DAO assigns each Facilitator a Bucket with a specified capacity, where a Bucket represents the upward limit of GHO that a specific Facilitator can mint. This limit is defined by Aave Governance.

### Governance

The Aave Protocol is a fully decentralized, community-governed protocol, managed by AAVE (and stkAAVE) token holders. Token holders collectively discuss, propose, and vote on upgrades to the Aave Protocol through Aave [Governance](gho-governance.md). AAVE and stkAAVE token holders (Ethereum network only) can either vote on new proposals or delegate their voting power to an address of choice.

### Risk Management and Mitigations

As is typical with all smart contracts built by the Aave Companies, there has been a focus on [risk management and mitigation](./risk-man-mitigations.md) for GHO.

## Fundamental Concepts

These pages show the different mechanisms involved with GHO, such as how to [borrow](../fundamental-concepts/borrow-gho.md) and [repay](../fundamental-concepts/repay-liquidate-gho.md) GHO, how [staking benefits](../fundamental-concepts/gho-discount-strategy.md) users, [arbitrage](../fundamental-concepts/arbitrage.md), and how to [FlashMint](../fundamental-concepts/flashmint.md).

## Smart Contracts

These pages dive into the GHO smart contracts to [explore GHO at a deeper](../../developer-docs/developer-docs-overview.md), technical level. The code design includes software-based mechanisms for the emission and destruction of GHO, for controlling the stability of GHO, and for the role of Aave Governance and Facilitators in managing and maintaining GHO.

## Resources

For [more information](../../resources/resources.md) please see the GHO Glossary, audits, and community resources.

----
docs/concepts/how-gho-works/interest-rate-discount-model.md
---
sidebar_position: 2
---

# Interest and Discount Rate Models

## Interest Rate Model

Compared to other assets within the Aave Protocol, GHO smart contracts do not follow the usual supply and demand dynamics that can often impact interest rates.

For GHO, the Aave Protocol integration requires interest rates to be determined by a coordination entity, specifically [Aave Governance](https://governance.aave.com/). The interest rates are set by Aave Governance, which statically adjusts interest rates depending on the need for the GHO supply to contract or expand.

Any changes to the interest rates require a governance proposal. This design works as a stability mechanism and retains the Aave Protocol’s borrow interest rate model flexibility. It will be possible in the future to implement any interest rate strategy the Aave Governance community sees fit.

### Interest Rates

The interest rate is the cornerstone of GHO stability, and, as in all decentralized protocols, it is built into the code.

The GHO price is fixed to $1 on the Aave Protocol; however, the price of GHO can be different in other markets (please see the [Arbitrage](../fundamental-concepts/arbitrage.md) page for further information). When this happens, Aave Governance can vote to increase or decrease the interest rates to encourage users to mint GHO or repay their GHO.

### GHO Price is Above 1 Dollar

If the market price of GHO is above 1 USD, Aave Governance can decrease the interest rate, as a lower interest rate may encourage additional users to access GHO.

### GHO Price is Below 1 Dollar

If the market price of GHO is below 1 USD, Aave Governance can increase the interest rate. This encourages more users to pay back their GHO positions which will decrease the outstanding GHO supply.

## Discount Rate Model

Given the nature of the asset, this integration allows for innovative features that provide greater utility for Aave Governance and community participants. The implementation of GHO includes a [Discount Strategy](../fundamental-concepts/gho-discount-strategy.md) mechanism, which allows for Safety Module participants (i.e., stkAAVE holders) to access a discount on the GHO borrow rate. The strategy sets a certain amount of GHO at discount per stkAAVE supplied and a discount on the interest rates that can vary from 0% (i.e., no discount) to 100% (i.e., full discount).

Discounts are available to borrowers staking AAVE in the Safety Module, which is a smart contract-based risk mitigation tool that is leveraged in the event of a shortfall event. By contributing to the Safety Module, users assume the risk that their stake will be slashed to cover the deficit in the event of bad debt arising in the Aave Protocol. To incentivize users to participate in staking and reward them for assuming this risk, users staking AAVE can receive a discount on their interest rate.

The configuration of the discount rate is controlled by Aave Governance.

### For each stkAAVE there will be a discount on the borrowing rate for 100 GHO

:::info

The parameters provided below are examples only. The initial parameters for the interest rate and discount model are subject to community discussions and a voting.

:::

For each stkAAVE, a user can receive a 50% discount on interest for 100 GHO, at an interest rate of 3%. If a user stakes 1 AAVE and borrows 100 GHO, they have borrowed the maximum amount of GHO available to them at a discount. Their interest rate is 50% of 3% → 1.5%. If a user instead borrows 200 GHO, 100 of that GHO will be at a 1.5% interest rate and 100 of the GHO will be at a 3% interest rate. Their effective interest rate will be 2.25%.

:::caution

The example above provides a simplified example of the discount rate for stkAAVE holders. Please see [GHO Discount Strategy](../fundamental-concepts/gho-discount-strategy.md) for detailed implementation.

:::

## Discount Rate Changes

The discount model is designed to be updated easily. Therefore, if Aave Governance determines that a different strategy is required, it can be implemented efficiently.

The discount rate is always available to a user but can only be locked for a certain period of time.

When a user receives a discount, it is assigned to them and can be locked for a certain time period (e.g., 6 months). After the 6 months have passed, if Aave Governance has set a new discount strategy and the user receives another discount rate, it may not be the same as it will have changed to the rate updated by Aave Governance.

This may also happen if a user triggers a discount update, such as borrowing and repaying GHO and updating their stkAAVE balance.

Please see the [Discount Rate Strategy](../fundamental-concepts/gho-discount-strategy.md) page for more information on the technical implementation of the discount rate.

----
docs/concepts/how-gho-works/_category_.json
{
  "label": "How GHO works",
  "position": 2,
  "link": {
    "type": "generated-index"
  }
}
----
docs/concepts/how-gho-works/risk-man-mitigations.md
---
sidebar_position: 4
---

# Risk Management and Mitigations

## Collateral Asset Risk

The Aave DAO controls the collateral assets listed in the Aave pool as well as their configuration.

Risk contributors provide world-class risk management services to the Aave DAO including consultation and advanced market simulation data to inform the Aave DAO’s decisions. The Aave Protocol has historically taken a conservative and effective approach to managing and setting the configurations around the assets that are used for collateral on the protocol.

## Flash Crash Conditions

The exposure and risk of a flash crash exist in all markets; however, the Aave Protocol has proven to be a resilient market through abrupt, severe volatility in the past. With the same collateral requirements, liquidation process, and liquidator community, GHO inherits key risk mitigation properties from the Aave pool.

## Smart Contract Risk

GHO has been developed with security as a top priority. GHO has been reviewed as thoroughly as possible before being activated by Aave Governance. There is an active [bug bounty](https://github.com/aave/gho-bug-bounty) where any security vulnerabilities can be reported and awarded the bounty if the criteria is met.

The system has been designed to be safe and secure and to meet the highest security standards. The GHO smart contracts have been developed following responsible development practices, which includes both internal and external code reviews and formal verification from [auditors](../../resources/resources.md#audit-round-1) and community contributors.

Smart contract risk can never be eliminated completely; however, through conservative development processes, it can be reduced.

The audit reports and formal verification for GHO can be found on the [Resources](../../resources/resources.md) page.

## Stability Mechanism

The following stability mechanisms have been implemented to ensure that GHO is stable:

- Locked oracle pricing
- Governance set interest rates

Please see the "[GHO Implementation](gho-implementation.md)" page for explanations of the stability mechanisms.

----
docs/concepts/how-gho-works/gho-implementation.md
---
sidebar_position: 1
---

# GHO Implementation

While interacting with GHO is similar to interacting with other assets within the Aave Protocol, the implementation of and user interaction with GHO as an asset in the Aave pool is quite different. The way that GHO is configured has differences that help it to maintain price stability.

## GHO is minted and burned by the smart contracts on demand when a user borrows and repays, respectively

GHO is not supplied to the Aave pool.

### Other Assets

All other assets must be supplied to the Aave Protocol by users, and only once supplied, can they be borrowed from the reserve. For example, if a user deposits USDC and would like to borrow LINK, another user must have supplied LINK for the user to later borrow it.

This is not required for GHO.

### GHO

If a user supplies USDC and would like to borrow GHO, there is no requirement for a user to have supplied GHO. Instead, the Aave Protocol calls the GHO contract mints GHO on demand. When repaying GHO debt, GHO is burned via smart contracts when the amount repaid exceeds the interest to pay, rather than going back to the suppliers.

This provides more flexibility than regular assets in the pool as GHO is minted on demand, the user does not have to rely on assets being supplied.

Facilitators will have the ability to mint GHO. Please see the [Facilitators](gho-facilitators.md) page to read about the role that Facilitators play for GHO.

## The GHO Oracle Price is Fixed at One U.S. Dollar

No matter what the market price is, the Aave Protocol will always value 1 GHO at the equivalent value of 1 USD, regardless of market price. This helps to maintain stability.

As the price is fixed, it creates immediate opportunities to help GHO maintain its peg.

For example, when the GHO price is above the peg, users can mint 1 GHO for $1 worth of debt. If the price of GHO is above $1 in the market, users can sell GHO for more than $1. This increases the supply of GHO while decreasing the asset price. The minter can later repay their debt at $1 while keeping the difference of what they sold GHO for. When the price of GHO is below the peg, minters can acquire 1 GHO on the market for less than $1 and pay off $1 worth of debt. This action shrinks the supply of GHO while increasing the asset price.

GHO is an over-collateralized asset, where every GHO is backed by more than $1 of collateral. This model has proved its resilience in the DeFi ecosystem for years.

## Interest Rates are Defined by Aave Governance

GHO borrow interest and discount rates are set by the Aave DAO. Aave Governance can periodically set the interest rates to help maintain stability with supply and demand.

### Other Assets

For a normal reserve within the Aave Protocol, interest rates are based on the utilization of that reserve. For example, if 10% of the supplied assets are borrowed, there will be a low-interest rate. If 90% of the supplied assets are borrowed, there will be a high-interest rate.

With GHO, there are no suppliers, which means that interest rates work differently.

### GHO

The interest rate is stable and will be adapted periodically depending on market conditions by Aave Governance to help control price stability. If the price of GHO increases, the interest rate should decrease to encourage the creation of GHO (i.e., GHO supply expands -> GHO rebalances down). If the GHO price decreases, the interest rate should increase to incentivize repayment (i.e., GHO supply contracts -> GHO prices rebalance up).

Please see the [Interest and Discount Rates](interest-rate-discount-model.md) page for more information.

## Repaid Interest is Re-directed to the Aave DAO Rather Than to Suppliers

### Other Assets

Normally, most of the interest earned on borrowed crypto assets is directed to the users that supplied the corresponding asset, and a small amount of this is directed to the Aave DAO.

### GHO

If GHO is not supplied, there are no suppliers to pay and therefore GHO does not have a reserve. All the interest accrued on positions will be paid to the Aave DAO.

## Facilitators

If approved by the Aave community, the [Aave V3 Ethereum Pool](./gho-facilitators.md#aave-v3-ethereum-pool) and [FlashMinter](./gho-facilitators.md#flashminter) Facilitator will be the first Facilitators on Ethereum Mainnet. In the future, there may be other Facilitators. Facilitators will have the ability to mint GHO and will be able to apply different strategies to their generation of GHO.

### Collateral

All assets that are enabled for use as collateral on the Aave Protocol can be used to back GHO.

### Liquidations

GHO works in the same way as assets already on the Aave Protocol. If the value of users’ collateral drops due to market conditions and their health factors decrease, liquidations can occur.

### Flashloan

GHO can be [FlashMinted](../fundamental-concepts/flashmint.md) via the FlashMinter Facilitator. This provides the same functionality as a flashloan in the current Aave pool; however, it is implemented differently from how flashloans are integrated today.

### Isolation Mode

[Isolation mode](https://docs.aave.com/developers/whats-new/isolation-mode) on V3 Aave Governance can limit exposure to the amount of GHO that can be minted based on collateral from riskier assets. If the community determines that a specific asset weight in GHO collateral is ‘too high,’ limits can be changed by a governance vote as Aave Governance sees fit. In this example, isolation mode reduces risk and keeps GHO collateralized.

### Bridges

Bridging support and logic will be dependent upon bridges that will support GHO.

----
docs/developer-docs/contracts-overview.md
---
id: contracts-overview
title: GHO Contracts
---

## Deployments

- [Goerli Deployment - GHO Community Testnet](#goerli-gho-deployment)
- [Sepolia Deployment - GHO Community Testnet](#sepolia-gho-deployment)


### Goerli Deployment - GHO Community Testnet {#goerli-gho-deployment}

Source code: https://github.com/aave/gho-core/pull/242/commits/c0999cb908d1037bb0515b88eb3cf15321cd3d60

| Name                                    | Address                                                                                                                      |
| :-------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| PoolAddressesProvider                   | [0x4dd5ab8Fb385F2e12aDe435ba7AFA812F1d364D0](https://goerli.etherscan.io/address/0x4dd5ab8Fb385F2e12aDe435ba7AFA812F1d364D0) |
| Pool-Proxy                              | [0x617Cf26407193E32a771264fB5e9b8f09715CdfB](https://goerli.etherscan.io/address/0x617Cf26407193E32a771264fB5e9b8f09715CdfB) |
| UiIncentiveDataProviderV3               | [0xF67B25977cEFf3563BF7F24A531D6CEAe6870a9d](https://goerli.etherscan.io/address/0xF67B25977cEFf3563BF7F24A531D6CEAe6870a9d) |
| UiPoolDataProviderV3                    | [0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52](https://goerli.etherscan.io/address/0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52) |
| ACLManager                              | [0x9C94757E231AdF6c90f89259DFA0841a1bf8172f](https://goerli.etherscan.io/address/0x9C94757E231AdF6c90f89259DFA0841a1bf8172f) |
| AaveOracle                              | [0xcb601629B36891c43943e3CDa2eB18FAc38B5c4e](https://goerli.etherscan.io/address/0xcb601629B36891c43943e3CDa2eB18FAc38B5c4e) |
| PoolConfigurator-Proxy                  | [0x04eA6B2a9E82Bd58bC95B8eA2b90496356dD969F](https://goerli.etherscan.io/address/0x04eA6B2a9E82Bd58bC95B8eA2b90496356dD969F) |
| PoolAddressesProviderRegistry           | [0x9B0FCD353468Eb9002bbF7cEA04e7EdA3AC188Ed](https://goerli.etherscan.io/address/0x9B0FCD353468Eb9002bbF7cEA04e7EdA3AC188Ed) |
| SupplyLogic                             | [0xae56b52ce982f6931783D35973EAb0cF71ee40a8](https://goerli.etherscan.io/address/0xae56b52ce982f6931783D35973EAb0cF71ee40a8) |
| BorrowLogic                             | [0xACf4be18be7D4eA90851f90A2816c2022bc5f9D0](https://goerli.etherscan.io/address/0xACf4be18be7D4eA90851f90A2816c2022bc5f9D0) |
| LiquidationLogic                        | [0xc428e1F850230a9F8B5f01301ea911c6df631ae1](https://goerli.etherscan.io/address/0xc428e1F850230a9F8B5f01301ea911c6df631ae1) |
| EModeLogic                              | [0xF7Ff469aAe15970f93e78Ec9e213e3b888B90179](https://goerli.etherscan.io/address/0xF7Ff469aAe15970f93e78Ec9e213e3b888B90179) |
| BridgeLogic                             | [0x7248a8Aaab397846CF6AA2B2E63CcdbBd771Bb06](https://goerli.etherscan.io/address/0x7248a8aaab397846cf6aa2b2e63ccdbbd771bb06) |
| ConfiguratorLogic                       | [0x16563750F712a218f8747Ae5681fD27f8665D645](https://goerli.etherscan.io/address/0x16563750F712a218f8747Ae5681fD27f8665D645) |
| FlashLoanLogic                          | [0xD290dDEf7D981d412DCBB56321FFD2a10aAb4A62](https://goerli.etherscan.io/address/0xD290dDEf7D981d412DCBB56321FFD2a10aAb4A62) |
| PoolLogic                               | [0x1687724da566D868D43a4163d741E156E74901DF](https://goerli.etherscan.io/address/0x1687724da566D868D43a4163d741E156E74901DF) |
| TreasuryProxy                           | [0x1A47958e231848C664863D213bC27b018934477D](https://goerli.etherscan.io/address/0x1A47958e231848C664863D213bC27b018934477D) |
| Treasury-Controller                     | [0x32ceB13aDe3D8B6951Fd00cE3cFaB6B7204B3d68](https://goerli.etherscan.io/address/0x32ceB13aDe3D8B6951Fd00cE3cFaB6B7204B3d68) |
| Treasury-Implementation                 | [0xbC3D79539C63E1372537527A3d882b2b81fD959c](https://goerli.etherscan.io/address/0xbC3D79539C63E1372537527A3d882b2b81fD959c) |
| Faucet                                  | [0x1265305F033156bbF8Ba54fE45DD5685BEc4Cc44](https://goerli.etherscan.io/address/0x1265305F033156bbF8Ba54fE45DD5685BEc4Cc44) |
| StakeAave-Proxy                         | [0xb85B34C58129a9a7d54149e86934ed3922b05592](https://goerli.etherscan.io/address/0xb85B34C58129a9a7d54149e86934ed3922b05592) |
| StakeAave-REV-1-Implementation          | [0x5A64c27c6d80eDC04DDCd47535E3aAfd37710f4F](https://goerli.etherscan.io/address/0x5A64c27c6d80eDC04DDCd47535E3aAfd37710f4F) |
| StakeAave-REV-2-Implementation          | [0xc6Bd39c5Eb353723Bbbd53ffAB47e75EE20fc197](https://goerli.etherscan.io/address/0xc6Bd39c5Eb353723Bbbd53ffAB47e75EE20fc197) |
| StakeAave-REV-3-Implementation          | [0xFD75CDBac86e3Da29fD9f0b3b0ED1A1eF347Dc49](https://goerli.etherscan.io/address/0xFD75CDBac86e3Da29fD9f0b3b0ED1A1eF347Dc49) |
| PoolDataProvider                        | [0xB7d8ff9949dB06D8387C28332045b8F734641755](https://goerli.etherscan.io/address/0xB7d8ff9949dB06D8387C28332045b8F734641755) |
| AAVE-TestnetPriceAggregator             | [0xFAa450873a4b162D32f545a85e678C13Ca8d4Ae9](https://goerli.etherscan.io/address/0xFAa450873a4b162D32f545a85e678C13Ca8d4Ae9) |
| DAI-TestnetPriceAggregator              | [0x3D9069811D8ABFaFBf16Fa07FC875E39D4dd29DA](https://goerli.etherscan.io/address/0x3D9069811D8ABFaFBf16Fa07FC875E39D4dd29DA) |
| USDC-TestnetPriceAggregator             | [0xb56b714beF6892Bb4b1C342557bb6a1dD3Cb8cb7](https://goerli.etherscan.io/address/0xb56b714beF6892Bb4b1C342557bb6a1dD3Cb8cb7) |
| WETH-TestnetPriceAggregator             | [0xD54126c116372F2D524eCfc8831E936C999a894B](https://goerli.etherscan.io/address/0xD54126c116372F2D524eCfc8831E936C999a894B) |
| LINK-TestnetPriceAggregator             | [0x1445d6061cd1Bf04b8301292f25E1D7d027CdE04](https://goerli.etherscan.io/address/0x1445d6061cd1Bf04b8301292f25E1D7d027CdE04) |
| Pool-Implementation                     | [0x02947bD4aDc7F0f8a162B04c39D6965b1CD8c19C](https://goerli.etherscan.io/address/0x02947bD4aDc7F0f8a162B04c39D6965b1CD8c19C) |
| PoolConfigurator-Implementation         | [0xfbCAdF5e18D0CdF16Da9B5C5056Ba67Dfa625Ad8](https://goerli.etherscan.io/address/0xfbCAdF5e18D0CdF16Da9B5C5056Ba67Dfa625Ad8) |
| ReservesSetupHelper                     | [0x969d947289840d6284E1D2EFBB27Ae0920A7D53f](https://goerli.etherscan.io/address/0x969d947289840d6284E1D2EFBB27Ae0920A7D53f) |
| EmissionManager                         | [0xC9f3b10c05a3e2a49F8165AC29b9275f85DE06cD](https://goerli.etherscan.io/address/0xC9f3b10c05a3e2a49F8165AC29b9275f85DE06cD) |
| IncentivesV2-Implementation             | [0xC1Ae238718a07CB8905E16bFbc8DCe5E52CebE35](https://goerli.etherscan.io/address/0xC1Ae238718a07CB8905E16bFbc8DCe5E52CebE35) |
| IncentivesProxy                         | [0x8688FEF353f4940061b4893d563de1C487Aa92Fd](https://goerli.etherscan.io/address/0x8688FEF353f4940061b4893d563de1C487Aa92Fd) |
| PullRewardsTransferStrategy             | [0x1bEBa913DCD423f71A9c964A35f39E46661E90f0](https://goerli.etherscan.io/address/0x1bEBa913DCD423f71A9c964A35f39E46661E90f0) |
| StakedTokenTransferStrategy             | [0x1A34998D0cC925709d60A36A95d0fD774688cE74](https://goerli.etherscan.io/address/0x1A34998D0cC925709d60A36A95d0fD774688cE74) |
| AToken                                  | [0x877880d5E01b483add2f3223B709a26b622F0852](https://goerli.etherscan.io/address/0x877880d5E01b483add2f3223B709a26b622F0852) |
| DelegationAwareAToken                   | [0x54472E4e254dc12d15e0862eaaafd3C828F375E9](https://goerli.etherscan.io/address/0x54472E4e254dc12d15e0862eaaafd3C828F375E9) |
| StableDebtToken                         | [0xEe27a567B18ef957dd2BFBE027F09Ea3ecC35722](https://goerli.etherscan.io/address/0xEe27a567B18ef957dd2BFBE027F09Ea3ecC35722) |
| VariableDebtToken                       | [0x80aa933EfF12213022Fd3d17c2c59C066cBb91c7](https://goerli.etherscan.io/address/0x80aa933EfF12213022Fd3d17c2c59C066cBb91c7) |
| ReserveStrategy-rateStrategyVolatileOne | [0x13Bdaf61b68b917114D4A356c2098D703D4C4aB7](https://goerli.etherscan.io/address/0x13Bdaf61b68b917114D4A356c2098D703D4C4aB7) |
| ReserveStrategy-rateStrategyStableOne   | [0xD740CB1d7c48795E32AcbA5c6A6b6E9ACBdD33F0](https://goerli.etherscan.io/address/0xD740CB1d7c48795E32AcbA5c6A6b6E9ACBdD33F0) |
| ReserveStrategy-rateStrategyStableTwo   | [0x4218E9D70F2fc2C44745E33DbfA7f7E90b19C783](https://goerli.etherscan.io/address/0x4218E9D70F2fc2C44745E33DbfA7f7E90b19C783) |
| AAVE-AToken                             | [0xAC4D92980562Ac11Af46C6C7CEdD7C819C2028D0](https://goerli.etherscan.io/address/0xAC4D92980562Ac11Af46C6C7CEdD7C819C2028D0) |
| AAVE-VariableDebtToken                  | [0xCB62E1d181179d1D86D3877e221D1EdE0bDD8841](https://goerli.etherscan.io/address/0xCB62E1d181179d1D86D3877e221D1EdE0bDD8841) |
| AAVE-StableDebtToken                    | [0x1721dDa383B02ec058Ee7B47596F61246eAD0069](https://goerli.etherscan.io/address/0x1721dDa383B02ec058Ee7B47596F61246eAD0069) |
| DAI-AToken                              | [0x7402b9625D1712426807952b798e3180dC38876F](https://goerli.etherscan.io/address/0x7402b9625D1712426807952b798e3180dC38876F) |
| DAI-VariableDebtToken                   | [0x76f5D888234e88599c12D46A2a55Fece923cf48c](https://goerli.etherscan.io/address/0x76f5D888234e88599c12D46A2a55Fece923cf48c) |
| DAI-StableDebtToken                     | [0x00b5314dcDA79F235a9EDE5dA53e63A9747c3f22](https://goerli.etherscan.io/address/0x00b5314dcDA79F235a9EDE5dA53e63A9747c3f22) |
| USDC-AToken                             | [0xdC916609281306558E0e8245bFBf90EFd3eCAb96](https://goerli.etherscan.io/address/0xdC916609281306558E0e8245bFBf90EFd3eCAb96) |
| USDC-VariableDebtToken                  | [0x908636F60d276a3b30C13F300065E1Cf43bf49cf](https://goerli.etherscan.io/address/0x908636F60d276a3b30C13F300065E1Cf43bf49cf) |
| USDC-StableDebtToken                    | [0x8117853a7Ecf500b27f5e5901c326B3840E58784](https://goerli.etherscan.io/address/0x8117853a7Ecf500b27f5e5901c326B3840E58784) |
| WETH-AToken                             | [0x49871B521E44cb4a34b2bF2cbCF03C1CF895C48b](https://goerli.etherscan.io/address/0x49871B521E44cb4a34b2bF2cbCF03C1CF895C48b) |
| WETH-VariableDebtToken                  | [0x86065184932b2e2E7bC2BC953Cd3d131d2497cDe](https://goerli.etherscan.io/address/0x86065184932b2e2E7bC2BC953Cd3d131d2497cDe) |
| WETH-StableDebtToken                    | [0xCEa68d3acD31b0d9d5E52f15Ce2662592C24aFc9](https://goerli.etherscan.io/address/0xCEa68d3acD31b0d9d5E52f15Ce2662592C24aFc9) |
| LINK-AToken                             | [0x601c61Fc4eEe64a4b1f5201125b788dc1585746b](https://goerli.etherscan.io/address/0x601c61Fc4eEe64a4b1f5201125b788dc1585746b) |
| LINK-VariableDebtToken                  | [0x91eFc3Ff5fBD2f9b2aE8880Bb1d52Db3e01A261d](https://goerli.etherscan.io/address/0x91eFc3Ff5fBD2f9b2aE8880Bb1d52Db3e01A261d) |
| LINK-StableDebtToken                    | [0x98413Db84158e6f4dEaa0F4d098240a7FdfA7060](https://goerli.etherscan.io/address/0x98413Db84158e6f4dEaa0F4d098240a7FdfA7060) |
| MockFlashLoanReceiver                   | [0x79A9D8009eFa62AE3C885aaD2a382c85FD90f87a](https://goerli.etherscan.io/address/0x79A9D8009eFa62AE3C885aaD2a382c85FD90f87a) |
| WrappedTokenGatewayV3                   | [0x9c402E3b0D123323F0FCed781b8184Ec7E02Dd31](https://goerli.etherscan.io/address/0x9c402E3b0D123323F0FCed781b8184Ec7E02Dd31) |
| WalletBalanceProvider                   | [0x03C8d0c46834921c4468C15A03E5d76Ae5CA3133](https://goerli.etherscan.io/address/0x03C8d0c46834921c4468C15A03E5d76Ae5CA3133) |
| UiIncentiveDataProviderV3               | [0xF67B25977cEFf3563BF7F24A531D6CEAe6870a9d](https://goerli.etherscan.io/address/0xF67B25977cEFf3563BF7F24A531D6CEAe6870a9d) |
| UiPoolDataProviderV3                    | [0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52](https://goerli.etherscan.io/address/0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52) |
| GhoToken                                | [0xcbE9771eD31e761b744D3cB9eF78A1f32DD99211](https://goerli.etherscan.io/address/0xcbE9771eD31e761b744D3cB9eF78A1f32DD99211) |
| GhoOracle                               | [0xDD714B0A68b9c81C6878688c5dc6238f8AC8eadD](https://goerli.etherscan.io/address/0xDD714B0A68b9c81C6878688c5dc6238f8AC8eadD) |
| UiGhoDataProvider                       | [0xeb939bA0D4CFA94a401569dD1056161ed2b49798](https://goerli.etherscan.io/address/0xeb939bA0D4CFA94a401569dD1056161ed2b49798) |
| GhoAToken                               | [0xdC25729a09241d24c4228f1a0C27137770cF363e](https://goerli.etherscan.io/address/0xdC25729a09241d24c4228f1a0C27137770cF363e) |
| StableDebtToken                         | [0x4461AC7d40EFBE8c9E37cC341dA380c57a9B2B78](https://goerli.etherscan.io/address/0x4461AC7d40EFBE8c9E37cC341dA380c57a9B2B78) |
| GhoVariableDebtToken                    | [0x7caBc754a0f1187b1A60BC9375508e07b362bDad](https://goerli.etherscan.io/address/0x7caBc754a0f1187b1A60BC9375508e07b362bDad) |
| GhoInterestRateStrategy                 | [0xF13b45F8FfF9342DC2b9EaD0D8442138ab8FA401](https://goerli.etherscan.io/address/0xF13b45F8FfF9342DC2b9EaD0D8442138ab8FA401) |
| GhoDiscountRateStrategy                 | [0xB82a29C9a83C52AbBc61327296B4Bb4Fa52050dA](https://goerli.etherscan.io/address/0xB82a29C9a83C52AbBc61327296B4Bb4Fa52050dA) |
| StakedTokenV2Rev4Impl                   | [0x324E0714991286d096723F2f24Ad20AAd3b5563A](https://goerli.etherscan.io/address/0x324E0714991286d096723F2f24Ad20AAd3b5563A) |
| GhoFlashMinter                          | [0x0cBf106fD14D1dFb320e7bfaA466FDCEC6471d46](https://goerli.etherscan.io/address/0x0cBf106fD14D1dFb320e7bfaA466FDCEC6471d46) |
| AaveStakingHelper                       | [0xe914d574975a1cd273388035db4413dda788c0e5](https://goerli.etherscan.io/address/0xe914d574975a1cd273388035db4413dda788c0e5) |
| StakeUIHelper                           | [0x02119C949D827ca1FaFFDb17B14E6A9dEE04f410](https://goerli.etherscan.io/address/0x02119C949D827ca1FaFFDb17B14E6A9dEE04f410) |

<br />

Goerli GHO Market Reserves

| Token                     | Address                                                                                                                      |
| :------------------------ | :--------------------------------------------------------------------------------------------------------------------------- |
| AAVE-TestnetMintableERC20 | [0xE205181Eb3D7415f15377F79aA7769F846cE56DD](https://goerli.etherscan.io/address/0xE205181Eb3D7415f15377F79aA7769F846cE56DD) |
| DAI-TestnetMintableERC20  | [0xD77b79BE3e85351fF0cbe78f1B58cf8d1064047C](https://goerli.etherscan.io/address/0xD77b79BE3e85351fF0cbe78f1B58cf8d1064047C) |
| USDC-TestnetMintableERC20 | [0x69305b943C6F55743b2Ece5c0b20507300a39FC3](https://goerli.etherscan.io/address/0x69305b943C6F55743b2Ece5c0b20507300a39FC3) |
| WETH-TestnetMintableERC20 | [0x84ced17d95F3EC7230bAf4a369F1e624Ae60090d](https://goerli.etherscan.io/address/0x84ced17d95F3EC7230bAf4a369F1e624Ae60090d) |
| LINK-TestnetMintableERC20 | [0x2166903C38B4883B855eA2C77A02430a27Cdfede](https://goerli.etherscan.io/address/0x2166903C38B4883B855eA2C77A02430a27Cdfede) |
| GhoToken                  | [0xcbE9771eD31e761b744D3cB9eF78A1f32DD99211](https://goerli.etherscan.io/address/0xcbE9771eD31e761b744D3cB9eF78A1f32DD99211) |

<br />

### Sepolia Deployment - GHO Community Testnet {#sepolia-gho-deployment}

Version: https://github.com/aave/gho-core/pull/242/commits/c0999cb908d1037bb0515b88eb3cf15321cd3d60

| Name                                    | Address                                                                                                                       |
| :-------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------- |
| PoolAddressesProvider                   | [0x6861730cFf157d3Ef3Fe987f526Ec5e1235B2f45](https://sepolia.etherscan.io/address/0x6861730cFf157d3Ef3Fe987f526Ec5e1235B2f45) |
| Pool-Proxy                              | [0xFF634a7b623E7e7ED49Cd6e9110b9F49b7Ef0Ec4](https://sepolia.etherscan.io/address/0xFF634a7b623E7e7ED49Cd6e9110b9F49b7Ef0Ec4) |
| UiPoolDataProviderV3                    | [0x25c682B532CFFDe7E2E657a4Dc9A277d87b5788C](https://sepolia.etherscan.io/address/0x25c682B532CFFDe7E2E657a4Dc9A277d87b5788C) |
| UiIncentiveDataProviderV3               | [0xA5c352032806D3F5935eEA7b67Dfe97eCfB0d7Cc](https://sepolia.etherscan.io/address/0xA5c352032806D3F5935eEA7b67Dfe97eCfB0d7Cc) |
| ACLManager                              | [0xBb3919fcF5338f338a0E900F121dbF7f70e1FbB6](https://sepolia.etherscan.io/address/0xBb3919fcF5338f338a0E900F121dbF7f70e1FbB6) |
| AaveOracle                              | [0xE952Af00cd4Bf5417bE2b590A313D02C4c35361c](https://sepolia.etherscan.io/address/0xE952Af00cd4Bf5417bE2b590A313D02C4c35361c) |
| PoolConfigurator-Proxy                  | [0x5f7808221c2CbBca65a3581b9509CFc279789FB2](https://sepolia.etherscan.io/address/0x5f7808221c2CbBca65a3581b9509CFc279789FB2) |
| BorrowLogic                             | [0x15405D8afA05f74b4a48FE15f876445958003264](https://sepolia.etherscan.io/address/0x15405D8afA05f74b4a48FE15f876445958003264) |
| BridgeLogic                             | [0x42EEAe12e924F4BEDA8d921F53488Cb232C5f853](https://sepolia.etherscan.io/address/0x42EEAe12e924F4BEDA8d921F53488Cb232C5f853) |
| ConfiguratorLogic                       | [0x9E35AF5E2aF6d4AAB8Ad4E1E0eD983A3E9291414](https://sepolia.etherscan.io/address/0x9E35AF5E2aF6d4AAB8Ad4E1E0eD983A3E9291414) |
| EModeLogic                              | [0x8a88Bb514FFC90C760A20b354A26468CBEC148e6](https://sepolia.etherscan.io/address/0x8a88Bb514FFC90C760A20b354A26468CBEC148e6) |
| FlashLoanLogic                          | [0xAf900986fA43c37a38325DfEDb7e8414c011E149](https://sepolia.etherscan.io/address/0xAf900986fA43c37a38325DfEDb7e8414c011E149) |
| LiquidationLogic                        | [0x8B7867d5bEd71BBD1852Ed5E6E49ebA03C0b02B2](https://sepolia.etherscan.io/address/0x8B7867d5bEd71BBD1852Ed5E6E49ebA03C0b02B2) |
| PoolAddressesProviderRegistry           | [0x7fBd08323FF00E3Ca2dD4EaeABa22C56C1fC17FC](https://sepolia.etherscan.io/address/0x7fBd08323FF00E3Ca2dD4EaeABa22C56C1fC17FC) |
| PoolLogic                               | [0x06797Ea3A61A832A88bB850D177833560bec922a](https://sepolia.etherscan.io/address/0x06797Ea3A61A832A88bB850D177833560bec922a) |
| StakeAave-Proxy                         | [0x47805f115eD9Dffc3506c9cB9805725FAe1cA9d3](https://sepolia.etherscan.io/address/0x47805f115eD9Dffc3506c9cB9805725FAe1cA9d3) |
| StakeAave-REV-1-Implementation          | [0x92D7540913a5F7DEa4E7a8F91dcCB6be39FC1aa9](https://sepolia.etherscan.io/address/0x92D7540913a5F7DEa4E7a8F91dcCB6be39FC1aa9) |
| StakeAave-REV-2-Implementation          | [0x8D613f634A8B198b8595998D33f28A94A8eBF3b2](https://sepolia.etherscan.io/address/0x8D613f634A8B198b8595998D33f28A94A8eBF3b2) |
| StakeAave-REV-3-Implementation          | [0x6BaA06079c274e28eee6ed635216663Bd72244F9](https://sepolia.etherscan.io/address/0x6BaA06079c274e28eee6ed635216663Bd72244F9) |
| SupplyLogic                             | [0xa157BF72450C55780Be145250B6b442d5B04cAcB](https://sepolia.etherscan.io/address/0xa157BF72450C55780Be145250B6b442d5B04cAcB) |
| Treasury-Controller                     | [0x4a3Bddb67ef9B9ddc8C96A5b3BdEf57d8E3d9abc](https://sepolia.etherscan.io/address/0x4a3Bddb67ef9B9ddc8C96A5b3BdEf57d8E3d9abc) |
| Treasury-Implementation                 | [0xd5a85B41848ebE7267A79b6A7Bd1a46628E80256](https://sepolia.etherscan.io/address/0xd5a85B41848ebE7267A79b6A7Bd1a46628E80256) |
| TreasuryProxy                           | [0x7A5364dc658a8B5920E07F4DDb54A6F128707409](https://sepolia.etherscan.io/address/0x7A5364dc658a8B5920E07F4DDb54A6F128707409) |
| Pool-Implementation                     | [0xf13da2ACbbc3bC9d517e5321Bd7C34CC72f0DE03](https://sepolia.etherscan.io/address/0xf13da2ACbbc3bC9d517e5321Bd7C34CC72f0DE03) |
| PoolConfigurator-Implementation         | [0x68628ddcdA6865627F41116ee28BD14AC3179f2B](https://sepolia.etherscan.io/address/0x68628ddcdA6865627F41116ee28BD14AC3179f2B) |
| ReservesSetupHelper                     | [0x2d09b7Faa27D10974f0c078EFa04087A1748A7B6](https://sepolia.etherscan.io/address/0x2d09b7Faa27D10974f0c078EFa04087A1748A7B6) |
| EmissionManager                         | [0xC9A008AaAaE5B8459E6f4D95B183de06e56459E0](https://sepolia.etherscan.io/address/0xC9A008AaAaE5B8459E6f4D95B183de06e56459E0) |
| IncentivesV2-Implementation             | [0xCf6f5277793eCB8ce4DE29F5117F572042a46348](https://sepolia.etherscan.io/address/0xCf6f5277793eCB8ce4DE29F5117F572042a46348) |
| IncentivesProxy                         | [0x15b0e99DB5cB98b35919DC8866F62adaA12aBB36](https://sepolia.etherscan.io/address/0x15b0e99DB5cB98b35919DC8866F62adaA12aBB36) |
| PullRewardsTransferStrategy             | [0x87F2fF7b4e37d42C70ed6eE4B7a9361f5810b003](https://sepolia.etherscan.io/address/0x87F2fF7b4e37d42C70ed6eE4B7a9361f5810b003) |
| Faucet                                  | [0xc1bFB9323bF7d2aE66e064A4d46FDD21e65464f3](https://sepolia.etherscan.io/address/0xc1bFB9323bF7d2aE66e064A4d46FDD21e65464f3) |
| StakedTokenTransferStrategy             | [0x8B3F24585021f28305b4D336C0C5432dcCa73D0D](https://sepolia.etherscan.io/address/0x8B3F24585021f28305b4D336C0C5432dcCa73D0D) |
| DelegationAwareAToken-Test              | [0x417B33a245fBcDE502007A26B944656776a3f430](https://sepolia.etherscan.io/address/0x417B33a245fBcDE502007A26B944656776a3f430) |
| ReserveStrategy-rateStrategyVolatileOne | [0xD2f5403725ba2c3300E1D0fD8D1B055540efC757](https://sepolia.etherscan.io/address/0xD2f5403725ba2c3300E1D0fD8D1B055540efC757) |
| ReserveStrategy-rateStrategyStableOne   | [0x78612Fcb888B195ABfc83a18a8dFFF8058960151](https://sepolia.etherscan.io/address/0x78612Fcb888B195ABfc83a18a8dFFF8058960151) |
| ReserveStrategy-rateStrategyStableTwo   | [0x56e32355b43926b4237FDDBE856183c44A8B93f3](https://sepolia.etherscan.io/address/0x56e32355b43926b4237FDDBE856183c44A8B93f3) |
| MockFlashLoanReceiver                   | [0x81E42Fa50636c405f9cea58bEd927031c7091EdE](https://sepolia.etherscan.io/address/0x81E42Fa50636c405f9cea58bEd927031c7091EdE) |
| WrappedTokenGatewayV3                   | [0xd45a6502E4d3e9e66829Bb07a4eB4f662873417b](https://sepolia.etherscan.io/address/0xd45a6502E4d3e9e66829Bb07a4eB4f662873417b) |
| WalletBalanceProvider                   | [0x894ef447CF3C97F267999244B1D130Bd746153E6](https://sepolia.etherscan.io/address/0x894ef447CF3C97F267999244B1D130Bd746153E6) |
| GhoToken                                | [0x5d00fab5f2F97C4D682C1053cDCAA59c2c37900D](https://sepolia.etherscan.io/address/0x5d00fab5f2F97C4D682C1053cDCAA59c2c37900D) |
| GhoOracle                               | [0xE6bD2F379D8C45DA43acc12d9fCCE7A70f02A480](https://sepolia.etherscan.io/address/0xE6bD2F379D8C45DA43acc12d9fCCE7A70f02A480) |
| GhoAToken                               | [0x204dC7Fa1040BD2106527753C3f2b9eE4c8c2e61](https://sepolia.etherscan.io/address/0x204dC7Fa1040BD2106527753C3f2b9eE4c8c2e61) |
| StableDebtToken                         | [0x1200b3265edEf57CA80f3e917BadEDe6e133159F](https://sepolia.etherscan.io/address/0x1200b3265edEf57CA80f3e917BadEDe6e133159F) |
| GhoVariableDebtToken                    | [0x6B93438eCA049E53cFE35007Df9276bb9985fcF2](https://sepolia.etherscan.io/address/0x6B93438eCA049E53cFE35007Df9276bb9985fcF2) |
| GhoInterestRateStrategy                 | [0xc7fb35995C25292A3764a19FF5B97fCd3310Fe3d](https://sepolia.etherscan.io/address/0xc7fb35995C25292A3764a19FF5B97fCd3310Fe3d) |
| GhoDiscountRateStrategy                 | [0xb6EEaFb1aDe5E47F8b411c6E386E2613c46D7121](https://sepolia.etherscan.io/address/0xb6EEaFb1aDe5E47F8b411c6E386E2613c46D7121) |
| StakedTokenV2Rev4Impl                   | [0x6005b38F31FB19a63Ea991e610D0b0b905567FA7](https://sepolia.etherscan.io/address/0x6005b38F31FB19a63Ea991e610D0b0b905567FA7) |
| GhoFlashMinter                          | [0x9664803466436AD9364CB897183B3b6D5ac4DDE7](https://sepolia.etherscan.io/address/0x9664803466436AD9364CB897183B3b6D5ac4DDE7) |
| UiGhoDataProvider                       | [0xCC3B9A84d5AbC04fb73B2a8Fa67Be4335d55D594](https://sepolia.etherscan.io/address/0xCC3B9A84d5AbC04fb73B2a8Fa67Be4335d55D594) |
| GhoManager                              | [0x4D485AcC40DB1152DF3E49dd553eeCc88a44abE7](https://sepolia.etherscan.io/address/0x4D485AcC40DB1152DF3E49dd553eeCc88a44abE7) |
| AaveStakingHelper                       | [0xbd885E8EfaE50CBfD43AC7155d8E0b5276aeB8ac](https://sepolia.etherscan.io/address/0xbd885E8EfaE50CBfD43AC7155d8E0b5276aeB8ac) |
| StakeUIHelper                           | [0x8a1c29681c0b01d09ed5487418A812C7b6924BBf](https://sepolia.etherscan.io/address/0x8a1c29681c0b01d09ed5487418A812C7b6924BBf) |

<br />

GHO Sepolia Market Reserves

| Name                           | Address                                                                                                                            |
| :------------------------------| :--------------------------------------------------------------------------------------------------------------------------------- |
| AAVE-TestnetMintableERC20      | [0xf9aBBc6E64f3Cb3cb237EbcAB95A252365BBd0D0](https://sepolia.etherscan.io/address/0xf9aBBc6E64f3Cb3cb237EbcAB95A252365BBd0D0)      |
| DAI-TestnetMintableERC20       | [0xe5118E47e061ab15Ca972D045b35193F673bcc36](https://sepolia.etherscan.io/address/0xe5118E47e061ab15Ca972D045b35193F673bcc36)      |
| LINK-TestnetMintableERC20      | [0xe97aacf2F1248484003d3208CF4060ec262c6b03](https://sepolia.etherscan.io/address/0xe97aacf2F1248484003d3208CF4060ec262c6b03)      |
| USDC-TestnetMintableERC20      | [0xEbCC972B6B3eB15C0592BE1871838963d0B94278](https://sepolia.etherscan.io/address/0xEbCC972B6B3eB15C0592BE1871838963d0B94278)      |
| WETH-TestnetMintableERC20      | [0xA1A245cc76414DC143687D9c3DE1152396f352D6](https://sepolia.etherscan.io/address/0xA1A245cc76414DC143687D9c3DE1152396f352D6)      |
| GhoToken                       | [0x5d00fab5f2F97C4D682C1053cDCAA59c2c37900D](https://sepolia.etherscan.io/address/0x5d00fab5f2F97C4D682C1053cDCAA59c2c37900D)      |
----
docs/developer-docs/_category_.json
{
  "label": "Developer Docs",
  "position": 4,
  "link": {
    "type": "generated-index"
  }
}
----
docs/developer-docs/developer-docs-overview.md
---
id: overview
title: Developer Docs
sidebar_position: 1
---

import AaveGhostSrc from "@site/static/img/Aave_ghost.png";

<div className="ghost-container">
  <img className="ghost-image" src={AaveGhostSrc} alt="aave ghost" />
</div>

<h1 className="builders-title">GHO is for builders</h1>

<div className="button-group">
<a href="#learn-gho">
    <button className="clickable-button">Learn GHO</button>
</a>

<a href="#integrate-gho">
    <button className="clickable-button">Integrate GHO</button>
</a>
</div>

### Quick Links

- <a className="links-list" href="contracts-overview">
    Deployed GHO Contracts
  </a>
- <a className="links-list" href="https://github.com/aave/gho-core">
    GHO Contract Source Code
  </a>
- <a
  className="links-list"
  href="https://docs.aave.com/developers/deployed-contracts/deployed-contracts"
  > Deployed Aave Protocol Contracts
  </a>
- <a className="links-list" href="https://github.com/aave/aave-v3-core">
    Aave V3 Contract Source Code
  </a>
- <a className="links-list" href="#gho-sdk">
    GHO JavaScript SDK
  </a>
- <a
  className="links-list"
  href="https://github.com/bgd-labs/aave-address-book"
  > Solidity and JavaScript Address Registry
  </a>

## Learn GHO

- a. [Aave V3 Ethereum Pool Facilitator](#aave-v3-ethereum-pool-facilitator)
  1. [Mint](#minting)
  2. [Repay](#repay)
  3. [Liquidate](#liquidation)
- b. [FlashMinter Facilitator](#flashminter-facilitator)
- c. [Discount Dynamics](#discount-dynamics)

GHO is an ERC20 token minted from contracts designated as [Facilitators](../concepts/how-gho-works/gho-facilitators.md). It has been proposed to the Aave community that the [Aave V3 Ethereum Pool](../concepts/how-gho-works/gho-facilitators.md#aave-v3-ethereum-pool) and [FlashMinter](../concepts/how-gho-works/gho-facilitators.md#flashminter) Facilitator will be the first Facilitators of GHO.

The Aave Pool facilitator will facilitate the minting and burning of GHO through the standard `borrow` and `repay` function which are utilizaed by all other Aave reserves. The flashminter facilitator will provide flashloan functionality to GHO which is not available by default.

![GHO_Architecture Diagram](../assets/GHO_Architecture_dark.png#gh-dark-mode-only)
![GHO_Architecture Diagram](../assets/GHO_Architecture.png#gh-light-mode-only)

A Facilitator can trustlessly mint and burn GHO tokens through various strategies. The Aave DAO assigns each Facilitator a Bucket with a specified Capacity, which is the upward limit of GHO that a specific Facilitator can mint. This limit is defined and can be changed by the Aave DAO.

![Facilitator Diagram](../assets/facilitator_dark.png#gh-dark-mode-only)
![Facilitator Diagram](../assets/facilitator.png#gh-light-mode-only)

### Aave V3 Ethereum Pool Facilitator

Interacting with GHO via the Aave Pool Facilitator is very similar to interacting with a typical reserve asset. Below are the technical guides for all GHO actions along with their contract references.

### Minting

[Minting](../concepts/fundamental-concepts/borrow-gho.md) occurs through the `borrow()` function of the Pool where GHO is listed. To mint GHO, the process is identical to borrowing any other reserve. To mint, an address must have sufficient collateral which is performed by approving and then calling `supply()` on the Aave Pool with an eligible collateral asset. Once an address has sufficient collateral, it is able to borrow up to a maximum collateral factor determined by it's collateral asset composition.

GHO can be added to an eMode category, which modifies the collateral factor and liquidation threshold. This can be queried with the following fields from the [integrating GHO](#integrate-gho) section.

`reserve.eModeCategoryId`: id of eMode category reserve belongs to
`user.userEModeCategoryId`: user's active eMode category

Since GHO is created and not borrowed from suppliers, GHO is not subject to restrictions on available liquidity, and instead, the Facilitator cap and collateralization requirements define the limits to which GHO can be minted as calculated below.

`availableFacilitatorCap = ghoReserveData.aaveFacilitatorButcketMaxCapacity - ghoReserveData.aaveFacilitatorBucketLevel`

See [core functions](#core-functions) for GHO borrowing integrations.

### Repay

GHO is [repaid](../concepts/fundamental-concepts/repay-liquidate-gho.md) just like any other asset, by approving the Pool contract to spend GHO tokens (by approval transaction or [signed permit](https://github.com/aave/aave-utilities#signERC20Approval) and `repayWithPermit`).

What is different about GHO is the calculation of accrued interest. See the [discount dynamics](#discount-dynamics) section for more info on how accrued interest affects balances for repayment.

See [core functions](#core-functions) for GHO repay integrations.

### Liquidation

When an address has a GHO borrow position, they are eligible to be liquidated under the same conditions as any other collateralized address. If the health factor of a GHO borrow falls below one, which occurs when the sum of borrow value exceeds the weighted average of liquidation thresholds of collateral assets, then any address is eligible to make a `liquidationCall` on the Pool contract.

The `liquidationCall` repays up to 100% of the GHO borrow position in exchange for an equivalent USD valuation of the collateral plus a liquidation bonus.

See the developers [liquidation guide](https://docs.aave.com/developers/guides/liquidations) for more information.

### FlashMinter Facilitator

Since GHO is not borrowed like a typical Aave reserve, a separate Facilitator is used in place to replicate the `flashloan` functionality of the Aave Pool.

The FlashMinter Facilitator has a separate minting cap from the Aave Pool. Since all FlashMint transactions are returned in a single transaction, no GHO is ever minted against this Facilitator and the cap is applied to each transaction.

FlashMint is useful for a variety of applications such as liquidations, debt swaps, and peg arbitrage. More details on this Facilitator can be found [here](./flashmint-facilitator/GhoFlashMinter.md).

### Discount Dynamics

The [discount rate strategy](../concepts/fundamental-concepts/gho-discount-strategy) contract defines the parameters of a user's discount. The strategy can be updated by governance and the key parameters are a maximum discount percent (such as 20%), a discount token (such as stkAAVE), and an amount of gho borrowed at a discounted percent per discount token owned (such as 100 GHO per 1 stkAAVE).

The discount is not applied continuously as a GHO borrower accrues interest. Interest is compounded at the base borrow rate and the discount is applied when the borrow balance is queried by calling `balanceOf` directly or from an internal call such as `repay` or `liquidate`.

![GHO Discount Diagram](../assets/RepayAndLiquidateDark.png#gh-dark-mode-only)
![GHO DIscount Diagram](../assets/RepayAndLiquidate.png#gh-light-mode-only)

## Integrate GHO

GHO is operated on the public blockchain making it accessible to plug into any type of application.

The ability of an application to interact with the data and functionality of GHO is limited only by the connection to access the public blockchain.

Any Ethereum address can access the full functionality of GHO, and the real-time status and complete historical record of GHO transactions can be verified by anyone at any time.

This guide explains the best practices for integrating GHO into a variety of common application types.

1.  [Types of Integrations](#types-of-integrations)
    - a. [Smart Contracts](#smart-contracts)
    - b. [Frontend](#frontend)
    - c. [Data Analytics](#data-analytics)
2.  [GHO SDK](#gho-sdk)
    - a. [setup](#setup)
    - b. [borrow](#borrow)
    - c. [repay](#repay-1)
    - d. [FlashMint](#flashmint)
    - e. [Interface Live Data](#interface-live-data)
3.  [Data](#data)
    - a. [Live Data](#live-data)
    - b. [Historical Data](#historical-data)

## Types of Integrations

GHO can be integrated into virtually any application because all data and functionality occur through a public blockchain. This guide will give a tutorial on best practices for the most common categories of integration types

### Smart Contracts

Check out the [deployed GHO contracts](./contracts-overview.md) to get started with contract integrations.

### Frontend

[Aave Utilities](https://github.com/aave/aave-utilities) is a JavaScript SDK that can be used to greatly simplify the process of integrating GHO data and functionality.

It provides imports for fetching data, formatting data, and building transactions. Tutorials with sample code for utilizaing this SDK can be found [here](#gho-sdk)

### Data Analytics

The current state of GHO, and the complete historical record data are accessible to any application with blockchain querying capabilities. The contract addresses and ABIs for GHO contracts are available in the contract docs.

The [data](#data) section goes into detail about integrating the most common live and historical data queries for JavaScript and Python applications.

## GHO SDK

### setup

The [Aave Utilities Javascript SDK](https://github.com/aave/aave-utilities) is a utilty for fetching data and building transactions. Since GHO is under active development, it is not available in the main package versions. GHO versions are published from [this branch](https://github.com/aave/aave-utilities/pull/445) and the current version in use on the [GHO testnet app](https://gho.aave.com) are listed below:

```
npm install @aave/math-utils@1.13.6-b2b7613127eb1278aa61a20d618e3b6d95782bb2.0
npm install @aave/contract-helpers@1.13.6-b2b7613127eb1278aa61a20d618e3b6d95782bb2.0
```

or 

```
yarn add @aave/math-utils@1.13.6-b2b7613127eb1278aa61a20d618e3b6d95782bb2.0
yarn add @aave/contract-helpers@1.13.6-b2b7613127eb1278aa61a20d618e3b6d95782bb2.0
```

### borrow

GHO is minted through the `borrow` method of the Aave Pool facilitator which can be accessed from the `Pool` import of the contract-helpers package. The pre-requisite to `borrow` is that the address incurring the borrow position must have sufficient collateral. This is achieved by the caller supplying collateral or if the caller has been approved a credit delegation and passes in the delegators address in the `onBehalfOf` field.

<details>
<summary>Sample Code (JavaScript GHO SDK)</summary>

```js
import { Pool, InterestRate } from '@aave/contract-helpers';

const pool = new Pool(provider, {
  POOL: '0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52', // Goerli GHO market
  WETH_GATEWAY: '0x9c402E3b0D123323F0FCed781b8184Ec7E02Dd31', // Goerli GHO market
});

/*
- @param `user` The ethereum address that will receive the borrowed amount 
- @param `reserve` The ethereum address of the reserve asset 
- @param `amount` The amount to be borrowed, in human readable units (e.g. 2.5 ETH)
- @param `interestRateMode`//Whether the borrow will incur a stable (InterestRate.Stable) or variable (InterestRate.Variable) interest rate
- @param @optional `debtTokenAddress` The ethereum address of the debt token of the asset you want to borrow. Only needed if the reserve is ETH mock address 
- @param @optional `onBehalfOf` The ethereum address for which user is borrowing. It will default to the user address 
*/
const txs: EthereumTransactionTypeExtended[] = await pool.borrow({
  user,
  reserve: '0xcbE9771eD31e761b744D3cB9eF78A1f32DD99211', // Goerli GHO market
  amount,
  interestRateMode,
  debtTokenAddress: '0x80aa933EfF12213022Fd3d17c2c59C066cBb91c7', // Goerli GHO market
  onBehalfOf,
  referralCode,
});
```
Submit transaction using [these instructions](https://github.com/aave/aave-utilities#submitting-transactions).
</details>

### repay

Repay also occurs seamlessly through the `repay` function of the Aave V3 Pool contract. Since repay transfers assets, the Pool must be approved as a spender of the tokens. There are two routes for approval: 

- Approve via txn -> repay
- Approve via signed message -> repayWithPermit

There are instructions for both routes below:

<details>
<summary>Repay Sample Code (JavaScript GHO SDK)</summary>

```js
import { Pool } from '@aave/contract-helpers';

const pool = new Pool(provider, {
  POOL: '0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52', // Goerli GHO market
  WETH_GATEWAY: '0x9c402E3b0D123323F0FCed781b8184Ec7E02Dd31', // Goerli GHO market
});

/*
- @param `user` The ethereum address that will make the deposit 
- @param `reserve` The ethereum address of the reserve 
- @param `amount` The amount to be deposited 
- @param `interestRateMode` // Whether stable (InterestRate.Stable) or variable (InterestRate.Variable) debt will be repaid
- @param @optional `onBehalfOf` The ethereum address for which user is depositing. It will default to the user address
*/
const txs: EthereumTransactionTypeExtended[] = await pool.repay({
  user,
  reserve: '0xcbE9771eD31e761b744D3cB9eF78A1f32DD99211', // Goerli GHO market
  amount,
  interestRateMode,
  onBehalfOf,
});
```
Will return an array with repay transaction and optionally an approval transaction. Submit transaction(s) using [these instructions](https://github.com/aave/aave-utilities#submitting-transactions).
</details>

<details>
<summary>RepayWithPermit Sample Code (JavaScript GHO SDK)</summary>

```js
import { Pool } from '@aave/contract-helpers';

const pool = new Pool(provider, {
  POOL: '0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52', // Goerli GHO market
  WETH_GATEWAY: '0x9c402E3b0D123323F0FCed781b8184Ec7E02Dd31', // Goerli GHO market
});

// Generate payload to be signed by user
const approvalMsg = await pool.signERC20Approval({
   user,
   reserve,
   amount,
   deadline, // determined by you
  )
})

// User signs with wallet method such as ethers signTypedDataV4 and passed as signature variable in next call

/*
- @param `user` The ethereum address that will make the deposit 
- @param `reserve` The ethereum address of the reserve 
- @param `amount` The amount to be deposited 
- @param `interestRateMode` // Whether stable (InterestRate.Stable) or variable (InterestRate.Variable) debt will be repaid
- @param @optional `onBehalfOf` The ethereum address for which user is depositing. It will default to the user address
*/
const txs: EthereumTransactionTypeExtended[] = await pool.repayWithPermit({
  user,
  reserve: '0xcbE9771eD31e761b744D3cB9eF78A1f32DD99211', // Goerli GHO market
  amount,
  interestRateMode,
  onBehalfOf,
  signature,
});
```
Will return an array with repay transaction and optionally an approval transaction. Submit transaction(s) using [these instructions](https://github.com/aave/aave-utilities#submitting-transactions).

</details>

### flashmint

Coming soon to GHO SDK. In the meantime, can be accessed by following the [contracts documentation](./flashmint-facilitator/GhoFlashMinter.md). 

### Interface Live Data

There are several view contracts used to provide a summarized data source for market, incentives, and gho data. The utilities SDK exposes helper methods to fetch and format data from these contracts. To setup these packages see the [setup](#setup) section.

<details>
<summary>Sample Code (JavaScript GHO SDK)</summary>

```js
import { ethers } from 'ethers';
import { dayjs } from 'dayjs';
import {
  UiPoolDataProvider,
  UiIncentiveDataProvider,
  ChainId,
  GhoService,
} from '@aave/contract-helpers';
import {
  formatGhoReserveData,
  formatGhoUserData,
  formatReservesAndIncentives,
  formatUserSummaryAndIncentives,
} from '@aave/math-utils';

// ES5 Alternative imports
//  const {
//    ChainId,
//    UiIncentiveDataProvider,
//    UiPoolDataProvider,
//    GhoService,
//  } = require('@aave/contract-helpers');
//  const {
//    formatGhoReserveData,
//    formatGhoUserData,
//    formatReservesAndIncentives,
//    formatUserSummaryAndIncentives,
//  } = require('@aave/math-utils');
//  const ethers = require('ethers');

// Sample RPC address for querying ETH goerli
const provider = new ethers.providers.JsonRpcProvider(
  'https://eth-goerli.public.blastapi.io',
);

// User address to fetch data for, insert address here
const currentAccount = '0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c';

// View contract used to fetch all reserves data (including market base currency data), and user reserves
// Using Aave V3 Eth goerli address for demo
const poolDataProviderContract = new UiPoolDataProvider({
  uiPoolDataProviderAddress: '0x3De59b6901e7Ad0A19621D49C5b52cC9a4977e52', // Goerli GHO Market
  provider,
  chainId: ChainId.goerli,
});
const currentTimestamp = dayjs().unix()

// View contract used to fetch all reserve incentives (APRs), and user incentives
// Using Aave V3 Eth goerli address for demo
const incentiveDataProviderContract = new UiIncentiveDataProvider({
  uiIncentiveDataProviderAddress:
    '0xF67B25977cEFf3563BF7F24A531D6CEAe6870a9d', // Goerli GHO Market
  provider,
  chainId: ChainId.goerli,
});

const ghoService = new GhoService({
    provider,
    uiGhoDataProviderAddress: '0xE914D574975a1Cd273388035Db4413dda788c0E5', // Goerli GHO Market
});

async function fetchContractData() {
  // Object containing array of pool reserves and market base currency data
  // { reservesArray, baseCurrencyData }
  const reserves = await poolDataProviderContract.getReservesHumanized({
    lendingPoolAddressProvider: '0x4dd5ab8Fb385F2e12aDe435ba7AFA812F1d364D0', // Goerli GHO Market
  });

  // Object containing array or users aave positions and active eMode category
  // { userReserves, userEmodeCategoryId }
  const userReserves = await poolDataProviderContract.getUserReservesHumanized({
    lendingPoolAddressProvider: '0x4dd5ab8Fb385F2e12aDe435ba7AFA812F1d364D0', // Goerli GHO Market
    user: currentAccount,
  });

  // Array of incentive tokens with price feed and emission APR
  const reserveIncentives =
    await incentiveDataProviderContract.getReservesIncentivesDataHumanized({
      lendingPoolAddressProvider: '0x4dd5ab8Fb385F2e12aDe435ba7AFA812F1d364D0', // Goerli GHO Market
    });

  // Dictionary of claimable user incentives
  const userIncentives =
    await incentiveDataProviderContract.getUserReservesIncentivesDataHumanized({
      lendingPoolAddressProvider: '0x4dd5ab8Fb385F2e12aDe435ba7AFA812F1d364D0', // Goerli GHO Market
      user: currentAccount,
    });

   const ghoReserveData = await ghoService.getGhoReserveData();
   const ghoUserData = await ghoService.getGhoUserData(currentAccount);

  const formattedGhoReserveData = formatGhoReserveData({
    ghoReserveData,
  });
  const formattedGhoUserData = formatGhoUserData({
    ghoReserveData,
    ghoUserData,
    currentTimestamp,
  });

  const formattedPoolReserves = formatReservesAndIncentives({
    reserves: reserves.reservesData,
    currentTimestamp,
    marketReferenceCurrencyDecimals: reserves.baseCurrencyData.marketReferenceCurrencyDecimals,
    marketReferencePriceInUsd: reserves.baseCurrencyData.marketReferenceCurrencyPriceInUsd,
    reserveIncentives: reserveIncentives,
  })

  const userSummary = formatUserSummaryAndIncentives({
    currentTimestamp,
    marketReferencePriceInUsd: reserves.baseCurrencyData.marketReferenceCurrencyPriceInUsd,
    marketReferenceCurrencyDecimals: reserves.baseCurrencyData.marketReferenceCurrencyDecimals,
    userReserves: userReserves.userReserves,
    formattedReserves: formattedPoolReserves,
    userEmodeCategoryId: userReserves.userEmodeCategoryId,
    reserveIncentives: reserveIncentives,
    userIncentives: userIncentives,
  });

let formattedUserSummary = userSummary;
  // Factor discounted GHO interest into cumulative user fields
  if (formattedGhoUserData.userDiscountedGhoInterest > 0) {
    const userSummaryWithDiscount = formatUserSummaryWithDiscount({
      userGhoDiscountedInterest: formattedGhoUserData.userDiscountedGhoInterest,
      user,
      marketReferenceCurrencyPriceUSD: Number(
        formatUnits(reserves.baseCurrencyData.marketReferenceCurrencyPriceInUsd, USD_DECIMALS)
      ),
    });
    formattedUserSummary = {
      ...userSummary,
      ...userSummaryWithDiscount,
    };
  }

   console.log({ formattedGhoReserveData, formattedGhoUserData, formattedPoolReserves, formattedUserSummary });
}

fetchContractData();
```
</details>

<br />

## Data

All facilitator transactions occur through smart contracts, so querying the real-time state of facilitator and market data is possible through contract queries. The following guides will give sample code fetch live and historical data for GHO directly from contract queries and events.

### Live Data

To query live data for GHO, there are several view contracts which can give summarized information of markets, incentives, and gho data respectively:

- UiPoolDataProvider: Queries for all market and user data
- UiIncentiveDataProvider: QUeries for all available and user claimable incentives
- UiGhoDataProvider: Queries for Aave Pool facilitator and user discount

A complete example of fetching and formatting data from these contracts can be found in the GHO SDK [live data](#interface-live-data) section. These steps could also be adapted for other languages or use cases.

### Historical Data

Transactions of the GHO facilitator are queryable through events on the GHO contracts. In the future there will be indexed alternatives such as subgraphs, dashbaords, and tailored endpoints for GHO data, but for now this data is only through event queries. 

Shown below are 2 methods for generalized event queries using RPCs and the Etherscan API which can be used with the GHO deployed contracts to index historical data for GHO integrations.

Note: An archival node may be necessary for the rpcUrl to query historical events

<details>
<summary>Query Events RPC </summary>

```js
const { providers, Contract, utils } = require("ethers");
// REPLACE WITH YOUR DATA HERE
const abi = require("./yourAbi.json");
const contractAddress = "0x0";
const contractStartBlock = 1; // deployment block of the contract, to avoid filtering from genesis block
const rpcUrl = "https://eth-mainnet.public.blastapi.io"; // eth mainnet example
async function fetchEvents() {
  // Connect to an Ethereum node
  const provider = new providers.JsonRpcProvider("rpcUrk");
  // Create a Contract object
  const contract = new Contract(contractAddress, abi, provider);
  // Define the filter options
  const filter = {
    fromBlock: 0,
    toBlock: "latest",
    address: contractAddress,
  };
  // Get the events from the contract
  const events = await contract.provider.getLogs(filter);
  // Loop through the events and log them
  for (const event of events) {
    const eventJson = utils.parseLog(event);
    console.log(eventJson);
  }
}
fetchEvents();
```
</details>

<details>
<summary>Query Events Etherscan API</summary>

```js
const ethers = require("ethers");
const request = require("request-promise-native");
// REPLACE WITH YOUR DATA HERE
const abi = require("./yourAbi.json");
const contractAddress = "0x0";
const contractStartBlock = 1; // deployment block of the contract, to avoid filtering from genesis block
const ETHERSCAN_API_KEY = "";
async function fetchEvents() {
  // Set up the API key and base URL for the Etherscan API
  const baseUrl = "https://api.etherscan.io/api";
  const contractInterface = new ethers.utils.Interface(abi);
  // Set the initial page and block number
  let page = 1;
  let blockNumber = "latest";
  const PAGE_SIZE = 1000;
  // Loop through each transaction
  while (true) {
    // Set up the options for the API request
    const options = {
      url: `${baseUrl}`,
      qs: {
        module: "account",
        action: "txlist",
        address: contractAddress,
        startblock: contractStartBlock,
        endblock: blockNumber,
        page: page,
        sort: "asc",
        apikey: ETHERSCAN_API_KEY,
      },
      json: true,
    };
    // Send the API request
    const response = await request(options);
    for (const tx of response.result) {
      // Check if this transaction was sent to the contract
      if (tx.to.toLowerCase() === contractAddress.toLowerCase()) {
        // Add the transaction to the array
        const decodedData = contractInterface.decodeFunctionData(
          tx.input.slice(0, 10),
          tx.input
        );
        // Use decoded data here
      }
    }
    if (response.result.length < PAGE_SIZE) {
      break;
    } else {
      page += 1;
    }
  }
}
fetchEvents();
```
</details>
----
docs/developer-docs/GHO/_category_.json
{
  "label": "GHO",
  "position": 1,
  "link": {
    "type": "generated-index"
  }
}
----
docs/developer-docs/GHO/ERC20.md
# ERC20

This abstract contract is a gas-efficient ERC20 and EIP-2612 implementation. It is a modified version of [`Solmate ERC20`](https://github.com/transmissions11/solmate/blob/34d20fc027fe8d50da71428687024a29dc01748b/src/tokens/ERC20.sol) implementing the basic [`IERC20`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/IERC20.sol).

The contract is `ERC20` compliant and inherits the standard [`IERC20`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/IERC20.sol) interface.

This page is split up differently (than other contract pages) showing the public [metadata](#metadata-storage), [`ERC20`](#erc20-storage) and [`EIP-2612`](#eip-2612-storage) storage variables, and the [`ERC20`](#erc20-logic) and [`EIP-2612`](#eip-2612-logic) logic within the `ERC20` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/gho/ERC20.sol).

## Metadata Storage

### name

```solidity
string public name
```

The name of the token.

### symbol

```solidity
string public symbol
```

The symbol of the token.

### decimals

```solidity
uint8 public immutable decimals
```

The number of decimals the token uses.

## ERC20 Storage

### totalSupply

```solidity
uint256 public totalSupply
```

The total supply of tokens.

## EIP-2612 Storage

```solidity
bytes32 public constant PERMIT_TYPEHASH = keccak256(‘Permit(address owner,address spender,uint256 value,uint256 nonce,uint256 deadline)’)
```

## ERC20 Logic

### approve

```solidity
function approve(address spender, uint256 amount) public virtual returns (bool)
```

Allows the `spender` to withdraw from the account up to the `amount`.

#### Input Parameters:

| Name    | Type      | Description                                           |
| ------- | --------- | ----------------------------------------------------- |
| spender | `address` | The address of the user to approve to withdraw tokens |
| amount  | `uint256` | The amount of tokens the spender can withdraw         |

#### Return Values:

| Type   | Description                                                     |
| ------ | --------------------------------------------------------------- |
| `bool` | Returns true if the operation was successful, reverts otherwise |

### transfer

```solidity
function transfer(address to, uint256 amount) public virtual returns (bool)
```

Transfers the `amount` of tokens to the `to` address.

#### Input Parameters:

| Name   | Type      | Description                       |
| ------ | --------- | --------------------------------- |
| to     | `address` | The address to send the tokens to |
| amount | `unit256` | The amount of tokens to transfer  |

#### Return Values:

| Type   | Description                                                     |
| ------ | --------------------------------------------------------------- |
| `bool` | Returns true if the operation was successful, reverts otherwise |

### transferFrom

```solidity
function transferFrom(
    address from,
    address to,
    uint256 amount
) public virtual returns (bool)
```

Transfers the `amount` of tokens from the `from` address to the `to` address.

#### Input Parameters:

| Name   | Type      | Description                             |
| ------ | --------- | --------------------------------------- |
| from   | `address` | The address to transfer the tokens from |
| to     | `to`      | The address to transfer the tokens to   |
| amount | `uint256` | The amount of tokens to transfer        |

#### Return Values:

| Type   | Description                                                     |
| ------ | --------------------------------------------------------------- |
| `bool` | Returns true if the operation was successful, reverts otherwise |

## EIP-2612 Logic

### permit

```solidity
function permit(
    address owner,
    address spender,
    uint256 value,
    uint256 deadline,
    uint8 v,
    bytes32 r,
    bytes32 s
  ) public virtual
```

Allows a user to permit another account (or contract) to use their funds using a signed message. This enables gas-less transactions and single approval/transfer transactions. Allow passing a signed message to approve spending.

#### Input Parameters:

| Name     | Type      | Description                                                       |
| -------- | --------- | ----------------------------------------------------------------- |
| owner    | `address` | The owner of the funds                                            |
| spender  | `address` | The spender of the funds                                          |
| value    | `uint256` | The amount the spender is permitted to spend                      |
| deadline | `uint256` | The deadline timestamp, use type(uint256).max for max/no deadline |
| v        | `uint8`   | The V signature parameter                                         |
| r        | `bytes32` | The R signature parameter                                         |
| s        | `bytes32` | The S signature parameter                                         |

### DOMAIN_SEPARATOR

```solidity
function DOMAIN_SEPARATOR() public view virtual returns (bytes32)
```

Gets the domain separator for the token. Returns the cached value if the chainId matches cache, otherwise recomputes separator.

#### Return Values:

| Type      | Description                                        |
| --------- | -------------------------------------------------- |
| `bytes32` | The domain separator of the token at current chain |

----
docs/developer-docs/GHO/gho-token.md
# GhoToken

The `GhoToken` contract inherits the [`ERC20`](ERC20) and [`Ownable`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/access/Ownable.sol) contracts, and the [`IGhoToken`](./interfaces/IGhoToken) interface.

This page shows the external [write](#write-methods) and [view](#view-methods) methods within the `GhoToken` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/gho/GhoToken.sol).

## Write Methods

### mint

```solidity
function mint(address account, uint256 amount) external override
```

Mints the requested `amount` of tokens to the `account` address.

Only Facilitators with enough bucket capacity available can mint. The bucket level increases upon minting (`newBucketLevel = currentBucketLevel + amount`), and must be less than or equal to the bucket capacity.

Emits the [`FacilitatorBucketLevelUpdated`](./interfaces/IGhoToken.md#facilitatorbucketlevelupdated) event.
To track all Facilitator activity, follow this event.

#### Input Parameters:

| Name    | Type      | Description                          |
| ------- | --------- | ------------------------------------ |
| account | `address` | The address receiving the GHO tokens |
| amount  | `uint256` | The amount to mint                   |

### burn

```solidity
function burn(uint256 amount) external override
```

Burns the requested `amount` of tokens from the account address.

The amount of tokens to burn must be greater than 0.

Only active Facilitators (capacity > 0) can burn. The bucket level decreases upon burning (`newBucketLevel = currentBucketLevel - amount`).

Emits the [`FacilitatorBucketLevelUpdated`](./interfaces/IGhoToken.md#facilitatorbucketlevelupdated) event.

#### Input Parameters:

| Name   | Type      | Description        |
| ------ | --------- | ------------------ |
| amount | `uint256` | The amount to burn |

### addFacilitator

```solidity
function addFacilitator(
    address facilitatorAddress,
    Facilitator memory facilitatorConfig
) external onlyOwner
```

Add the Facilitator passed with the parameters to the Facilitators list.

The Facilitator must not have already been added and must have a [`label`](./interfaces/IGhoToken.md#facilitator). The bucket configuration must be valid, with the [`bucketLevel`](./interfaces/IGhoToken.md#facilitator) equal to 0.

Emits the [`FacilitatorAdded`](./interfaces/IGhoToken.md#facilitatoradded) event.

#### Input Parameters:

| Name               | Type          | Description                            |
| ------------------ | ------------- | -------------------------------------- |
| facilitatorAddress | `address`     | The address of the Facilitators to add |
| facilitatorConfig  | `Facilitator` | The configuration of the Facilitator   |

The [`Facilitator`](./interfaces/IGhoToken.md#facilitator) struct is composed of the following fields:

| Name     | Type      | Description                                                   |
| -------- | --------- | ------------------------------------------------------------- |
| capacity | `uint128` | The capacity of the bucket assigned to a specific Facilitator |
| level    | `uint128` | The bucket level                                              |
| label    | `string`  | The label of the Facilitator bucket                           |

### removeFacilitator

```solidity
function removeFacilitator(address facilitatorAddress) external onlyOwner
```

Remove the Facilitator from the Facilitators list.

The Facilitator must exist as a current Facilitator, and must have a [`bucketLevel`](./interfaces/IGhoToken.md#facilitator) equal to 0.

Emits the [`FacilitatorRemoved`](./interfaces/IGhoToken.md#facilitatorremoved) event.

#### Input Parameters:

| Name               | Type      | Description                               |
| ------------------ | --------- | ----------------------------------------- |
| facilitatorAddress | `address` | The address of the Facilitators to remove |

### setFacilitatorBucketCapacity

```solidity
function setFacilitatorBucketCapacity(address facilitator, uint128 newCapacity) external onlyOwner
```

Sets the bucket capacity for the `facilitator`.

The owner of the contract is able to increase/decrease the bucket capacity for the given `facilitator`.

Emits the [`FacilitatorBucketCapacityUpdated`](./interfaces/IGhoToken.md#facilitatorbucketcapacityupdated) event.

#### Input Parameters:

| Name        | Type      | Description                    |
| ----------- | --------- | ------------------------------ |
| facilitator | `address` | The address of the Facilitator |
| newCapacity | `uint128` | The new capacity of the bucket |

## View Methods

### getFacilitator

```solidity
function getFacilitator(address facilitator) external view returns (Facilitator memory)
```

Returns the `facilitator` data.

#### Input Parameters:

| Name        | Type      | Description                    |
| ----------- | --------- | ------------------------------ |
| facilitator | `address` | The address of the Facilitator |

#### Return Values:

| Type        | Description                   |
| ----------- | ----------------------------- |
| Facilitator | The Facilitator configuration |

The [`Facilitator`](./interfaces/IGhoToken.md#facilitator) struct is composed of the following fields:

| Name     | Type      | Description                                                   |
| -------- | --------- | ------------------------------------------------------------- |
| capacity | `uint128` | The capacity of the bucket assigned to a specific Facilitator |
| level    | `uint128` | The bucket level                                              |
| label    | `string`  | The label of the Facilitator bucket                           |

### getFacilitatorBucket

```solidity
function getFacilitatorBucket(address facilitator) external view returns (uint256, uint256)
```

Returns the `facilitator` bucket configuration.

#### Input Parameters:

| Name        | Type      | Description                    |
| ----------- | --------- | ------------------------------ |
| facilitator | `address` | The address of the Facilitator |

#### Return Values:

| Type      | Description                              |
| --------- | ---------------------------------------- |
| `uint128` | The capacity of the Facilitator’s bucket |
| `uint128` | The level of the Facilitator’s bucket    |

### getFacilitatorsList

```solidity
function getFacilitatorsList() external view returns (address[] memory)
```

Returns the list of addresses of the active Facilitators.

#### Return Values:

| Type        | Description                            |
| ----------- | -------------------------------------- |
| `address[]` | The list of the Facilitators addresses |

----
docs/developer-docs/GHO/GhoOracle.md
# GhoOracle

The price feed for GHO is fixed and denominated in USD. The price is fixed at 1 USD, using 8 decimals.

The Aave Protocol will be programmed to always use to price of 1 GHO = $1. This is different from using market pricing via oracles for other crypto assets. This creates stabilizing [arbitrage](../../concepts/fundamental-concepts/arbitrage) opportunities when the price of GHO fluctuates.

This page shows the public [constant state variables](#constant-state-variables), and [pure](#pure-methods) methods within the `GhoOracle` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/oracle/GhoOracle.sol).

## Constant State Variables

### GHO_PRICE

```solidity
int256 public constant GHO_PRICE = 1e8
```

Fixed at 1 USD, formatted with 8 decimals.

## Pure Methods

### latestAnswer

```solidity
function latestAnswer() external pure returns (int256)
```

Returns the [price](#ghoprice) of a unit of GHO (USD denominated).

The GHO price is fixed at 1 USD.

#### Return Values:

| Type     | Description                                  |
| -------- | -------------------------------------------- |
| `int256` | The price of a unit of GHO (with 8 decimals) |

### decimals

```solidity
function decimals() external pure returns (uint8)
```

Returns the number of decimals the price is formatted with, 8.

#### Return Values:

| Type    | Description               |
| ------- | ------------------------- |
| `uint8` | 8: the number of decimals |

----
docs/developer-docs/GHO/interfaces/IGhoFacilitator.md
# IGhoFacilitator

Interface to define the behavior of a GhoFacilitator. Designed to be implemented by Facilitators, to add common logic related to GHO Treasury.

This page shows the [events](#events), and [write](#write-methods) methods within the `IGhoFacilitator` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/gho/interfaces/IGhoFacilitator.sol).

## Events

### FeesDistributedToTreasury

```solidity
event FeesDistributedToTreasury(
    address indexed ghoTreasury,
    address indexed asset,
    uint256 amount
)
```

Emitted when fees are distributed to the GHO Treasury.

Emitted in the [`GhoAToken`](../../aave-facilitator/GhoAToken#distributefeestotreasury) and [`GhoFlashMinter`](../../flashmint-facilitator/GhoFlashMinter#distributefeestotreasury) contracts.

| Name        | Type      | Description                                             |
| ----------- | --------- | ------------------------------------------------------- |
| ghoTreasury | `address` | The address of the ghoTreasury                          |
| asset       | `address` | The address of the asset transferred to the ghoTreasury |
| amount      | `uint256` | The amount of the asset transferred to the ghoTreasury  |

### GhoTreasuryUpdated

```solidity
event GhoTreasuryUpdated(address indexed oldGhoTreasury, address indexed newGhoTreasury)
```

Emitted when the GHO Treasury address is updated.

Emitted in the [`GhoAToken`](../../aave-facilitator/GhoAToken#updateghotreasury) and [`GhoFlashMinter`](../../flashmint-facilitator/GhoFlashMinter#updateghotreasury) contracts.

## Write Methods

### distributeFeesToTreasury

```solidity
function distributeFeesToTreasury() external
```

Distribute fees to the GHO Treasury.

Facilitators may opt to delay the distribution of GHO fees to the treasury (i.e gas optimization) or on every user action making this function complementary or not necessary.

### updateGhoTreasury

```solidity
function updateGhoTreasury(address newGhoTreasury) external
```

Updates the address of the GHO Treasury.

:::caution

The GHO Treasury is where revenue fees are sent to. Update carefully.

:::

#### Input Parameters:

| Name           | Type      | Description                     |
| -------------- | --------- | ------------------------------- |
| newGhoTreasury | `address` | The address of the GHO Treasury |

### getGhoTreasury

```solidity
function getGhoTreasury() external view returns (address)
```

Returns the address of the GHO Treasury.

#### Return Values:

| Type      | Description                              |
| --------- | ---------------------------------------- |
| `address` | The address of the GHO Treasury contract |

----
docs/developer-docs/GHO/interfaces/IGhoToken.md
# IGhoToken

The interface of the [`GhoToken`](../gho-token.md).

The `IGhoToken` interface inherits the [`IERC20Burnable`](IERC20Burnable.md), [`IERC20Mintable`](IERC20Mintable.md), and [`IERC20`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/IERC20.sol) interfaces.

This page shows the [structs](#structs), [events](#events), and [write](#write-methods) and [view](#view-methods) methods within the `IGhoToken` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/gho/interfaces/IGhoToken.sol).

## Structs

### Facilitator

```solidity
struct Facilitator {
    uint128 bucketCapacity;
    uint128 bucketLevel;
    string label;
}
```

A `Facilitator` can trustlessly generate (and burn) GHO tokens.

| Name           | Type      | Description                                                   |
| -------------- | --------- | ------------------------------------------------------------- |
| bucketCapacity | `uint128` | The capacity of the bucket assigned to a specific Facilitator |
| bucketLevel    | `uint128` | The bucket level                                              |
| label          | `string`  | The label of the Facilitator bucket                           |

## Events

### FacilitatorAdded

```solidity
event FacilitatorAdded(
    address indexed facilitatorAddress,
    bytes32 indexed label,
    uint256 bucketCapacity
)
```

Emitted when a new Facilitator is [added](../gho-token.md#addfacilitator).

#### Input Parameters:

| Name               | Type      | Description                                            |
| ------------------ | --------- | ------------------------------------------------------ |
| facilitatorAddress | `address` | The address of the new Facilitator                     |
| label              | `bytes32` | A hashed human readable identifier for the Facilitator |
| bucketCapacity     | `uint256` | The initial capacity of the Facilitator’s bucket       |

### FacilitatorRemoved

```solidity
event FacilitatorRemoved(address indexed facilitatorAddress)
```

Emitted when a Facilitator is [removed](../gho-token.md#removefacilitator).

#### Input Parameters:

| Name               | Type      | Description                            |
| ------------------ | --------- | -------------------------------------- |
| facilitatorAddress | `address` | The address of the removed Facilitator |

### FacilitatorBucketCapacityUpdated

```solidity
event FacilitatorBucketCapacityUpdated(
    address indexed facilitatorAddress,
    uint256 oldCapacity,
    uint256 newCapacity
)
```

Emitted when the bucket capacity of a Facilitator is [updated](../gho-token.md#setfacilitatorbucketcapacity).

#### Input Parameters:

| Name               | Type      | Description                                                           |
| ------------------ | --------- | --------------------------------------------------------------------- |
| facilitatorAddress | `address` | The address of the Facilitator whose bucket capacity is being changed |
| oldCapacity        | `uint256` | The old capacity of the bucket                                        |
| newCapacity        | `uint256` | The new capacity of the bucket                                        |

### FacilitatorBucketLevelUpdated

```solidity
event FacilitatorBucketLevelUpdated(
    address indexed facilitatorAddress,
    uint256 oldLevel,
    uint256 newLevel
  )
```

Emitted when the bucket level has changed. This occurs when tokens have been [minted](../gho-token.md#mint) and [burned](../gho-token.md#burn).

#### Input Parameters:

| Name               | Type      | Description                                                        |
| ------------------ | --------- | ------------------------------------------------------------------ |
| facilitatorAddress | `address` | The address of the Facilitator whose bucket level is being changed |
| oldLevel           | `uint256` | The old level of the bucket                                        |
| newLevel           | `uint256` | The new level of the bucket                                        |

## Write Methods

### addFacilitator

```solidity
function addFacilitator(
    address facilitatorAddress,
    Facilitator memory facilitatorConfig
) external
```

Adds the Facilitator passed with the parameters to the Facilitators list.

#### Input Parameters:

| Name               | Type          | Description                           |
| ------------------ | ------------- | ------------------------------------- |
| facilitatorAddress | `address`     | The address of the Facilitator to add |
| facilitatorConfig  | `facilitator` | The configuration of the Facilitator  |

### removeFacilitator

```solidity
function removeFacilitator(address facilitatorAddress) external
```

Remove the Facilitator from the Facilitators list.

#### Input Parameters:

| Name               | Type      | Description                              |
| ------------------ | --------- | ---------------------------------------- |
| facilitatorAddress | `address` | The address of the Facilitator to remove |

### setFacilitatorBucketCapacity

```solidity
function setFacilitatorBucketCapacity(address facilitator, uint128 newCapacity) external
```

Set the bucket capacity of the `facilitator`.

#### Input Parameters:

| Name        | Type      | Description                    |
| ----------- | --------- | ------------------------------ |
| facilitator | `address` | The address of the Facilitator |
| newCapacity | `uint128` | The new capacity of the bucket |

## View Methods

### getFacilitator

```solidity
function getFacilitator(address facilitator) external view returns (Facilitator memory)
```

Returns the `facilitator` data.

#### Input Parameters:

| Name        | Type       | Description                    |
| ----------- | ---------- | ------------------------------ |
| facilitator | `address ` | The address of the Facilitator |

#### Return Values:

| Type          | Description                   |
| ------------- | ----------------------------- |
| `facilitator` | The Facilitator configuration |

### getFacilitatorBucket

```solidity
function getFacilitatorBucket(address facilitator) external view returns (uint256, uint256)
```

Returns the bucket configuration of the `facilitator`.

#### Input Parameters:

| Name        | Type      | Description                    |
| ----------- | --------- | ------------------------------ |
| facilitator | `address` | The address of the Facilitator |

#### Return Values:

| Type      | Description                              |
| --------- | ---------------------------------------- |
| `uint256` | The capacity of the Facilitator’s bucket |
| `uint256` | The level of the Facilitator’s bucket    |

### getFacilitatorsList

```solidity
function getFacilitatorsList() external view returns (address[] memory)
```

Returns the list of addresses of the active Facilitators.

#### Return Values:

| Type        | Description                            |
| ----------- | -------------------------------------- |
| `address[]` | The list of the Facilitators addresses |

----
docs/developer-docs/GHO/interfaces/_category_.json
{
  "label": "Interfaces",
  "link": {
    "type": "generated-index"
  }
}
----
docs/developer-docs/GHO/interfaces/IERC20Burnable.md
# IERC20Burnable

The interface of a burnable ERC20 token.

This page shows the [write](#write-methods) methods within the `IERC20Burnable` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/gho/interfaces/IERC20Burnable.sol).

## Write Methods

### burn

```solidity
function burn(uint256 amount) external
```

Destroys an `amount` tokens from the caller.

#### Input Parameters:

| Name   | Type      | Description                     |
| ------ | --------- | ------------------------------- |
| amount | `uint256` | The amount of tokens to destroy |

----
docs/developer-docs/GHO/interfaces/IERC20Mintable.md
# IERC20Mintable

The interface of a mintable ERC20 token.

This page shows the [write](#write-methods) methods within the `IERC20Mintable` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/gho/interfaces/IERC20Mintable.sol).

## Write Methods

### mint

```solidity
function mint(address account, uint256 amount) external
```

Creates an `amount` of new tokens for the `account` address.

#### Input Parameters:

| Name    | Type      | Description                      |
| ------- | --------- | -------------------------------- |
| account | `address` | The address to create tokens for |
| amount  | `uint256` | The amount of tokens to create   |

----
docs/developer-docs/flashmint-facilitator/_category_.json
{
  "label": "FlashMinter Facilitator",
  "link": {
    "type": "generated-index"
  }
}
----
docs/developer-docs/flashmint-facilitator/GhoFlashMinter.md
# GhoFlashMinter

This contract enables FlashMinting of GHO. It is based heavily on the [EIP3156](https://eips.ethereum.org/EIPS/eip-3156) reference implementation.

The `GhoFlashMinter` contract inherits the [`IGhoFlashMinter`](./interfaces/IGhoFlashMinter) interface.

This page shows the public [constant](#constant-state-variables) and [immutable](#immutable-state-variables) state variables, and external [write](#write-methods) and [view](#view-methods) methods within the `GhoFlashMinter` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/flashMinter/GhoFlashMinter.sol).

## Constant State Variables

### CALLBACK_SUCCESS

```solidity
bytes32 public constant CALLBACK_SUCCESS = keccak256('ERC3156FlashBorrower.onFlashLoan')
```

Hash of the `ERC3156FlashBorrower.onFlashLoan` that must be returned by the `onFlashLoan` callback.

### MAX_FEE

```solidity
  uint256 public constant MAX_FEE = 10000
```

The maximum percentage fee of the FlashMinted amount that the flashFee can be set to (in bps).

## Immutable State Variables

### ADDRESSES_PROVIDER

```solidity
IPoolAddressesProvider public immutable override ADDRESSES_PROVIDER
```

The address of the PoolAddressesProvider

## Write Methods

### flashLoan

```solidity
function flashLoan(
    IERC3156FlashBorrower receiver,
    address token,
    uint256 amount,
    bytes calldata data
) external override returns (bool)
```

Initiates a FlashMint. GHO is the only supported token.

From the [`IERC3156FlashLender`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/interfaces/IERC3156FlashLender.sol#L37) interface.

Emits the [`FlashMint`](./interfaces/IGhoFlashMinter#flashmint) event.

#### Input Parameters:

| Name     | Type                    | Description                                                              |
| -------- | ----------------------- | ------------------------------------------------------------------------ |
| receiver | `IERC3156FlashBorrower` | The receiver of the tokens in the loan, and the receiver of the callback |
| token    | `address`               | The loan currency. Only GHO is supported                                 |
| amount   | `uint256`               | The amount of tokens to FlashMint                                        |
| data     | `bytes`                 | Arbitrary data structure, intended to contain user-defined parameters    |

#### Return Values:

| Type   | Description                                                         |
| ------ | ------------------------------------------------------------------- |
| `bool` | Returns `true` if the operation was successful. If failed, reverts. |

### distributeFeesToTreasury

```solidity
function distributeFeesToTreasury() external virtual override
```

Distribute accumulated fees to the GHO treasury.

Emits the [`FeesDistributedToTreasury`](../GHO/interfaces/IGhoFacilitator.md#feesdistributedtotreasury) event.

### updateFee

```solidity
function updateFee(uint256 newFee) external onlyPoolAdmin
```

Updates the percentage fee. It is the percentage of the flash-minted amount that needs to be repaid. The fee is expressed in bps. A value of 100, results in 1.00%.

The `newFee` must be less than the [`MAX_FEE`](#max_fee).

Emits the [`FeeUpdated`](../flashmint-facilitator/interfaces/IGhoFlashMinter.md#feeupdated) event.

#### Input Parameters:

| Name   | Type      | Description                     |
| ------ | --------- | ------------------------------- |
| newFee | `uint256` | The new percentage fee (in bps) |

### updateGhoTreasury

```solidity
function updateGhoTreasury(address newGhoTreasury) external override onlyPoolAdmin
```

Updates the address of the GHO treasury, where FlashMint fees are sent.

Emits the [`GhoTreasuryUpdated`](../GHO/interfaces/IGhoFacilitator.md#ghotreasuryupdated) event.

#### Input Parameters:

| Name           | Type      | Description                    |
| -------------- | --------- | ------------------------------ |
| newGhoTreasury | `address` | The address of the GhoTreasury |

## View Methods

### maxFlashLoan

```solidity
function maxFlashLoan(address token) external view override returns (uint256)
```

The amount of currency available to be FlashMinted. GHO is the only supported token. Returns 0 if any other address other than GHO is passed.

From the [`IERC3156FlashLender`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/interfaces/IERC3156FlashLender.sol#L20) interface.

#### Input Parameters:

| Name  | Type      | Description             |
| ----- | --------- | ----------------------- |
| token | `address` | The loan currency (GHO) |

#### Return Values:

| Type      | Description                                  |
| --------- | -------------------------------------------- |
| `uint256` | The amount of token that can be FlashMinted. |

### flashFee

```solidity
function flashFee(address token, uint256 amount) external view override returns (uint256)
```

The fee to be charged for a given loan. GHO is the only supported token.

From the [`IERC3156FlashLender`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/interfaces/IERC3156FlashLender.sol#L28) interface.

#### Input Parameters:

| Name   | Type      | Description               |
| ------ | --------- | ------------------------- |
| token  | `address` | The loan currency         |
| amount | `uint256` | The amount of tokens lent |

#### Return Values:

| Type      | Description                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| `uint256` | The amount of token to be charged for the loan, on top of the returned principal |

### getFee

```solidity
function getFee() external view returns (uint256)
```

Returns the percentage of each flash mint taken as a fee.

#### Return Values:

| Type      | Description                                                                                            |
| --------- | ------------------------------------------------------------------------------------------------------ |
| `uint256` | The percentage fee of the FlashMinted amount that needs to be repaid, on top of the principal (in bps) |

### getGhoTreasury

```solidity
function getGhoTreasury() external view returns (address)
```

Returns the address of the GHO treasury.

#### Return Values:

| Type      | Description                             |
| --------- | --------------------------------------- |
| `address` | The address of the GhoTreasury contract |

----
docs/developer-docs/flashmint-facilitator/interfaces/_category_.json
{
  "label": "Interfaces",
  "position": 3,
  "link": {
    "type": "generated-index"
  }
}

----
docs/developer-docs/flashmint-facilitator/interfaces/IGhoFlashMinter.md
# IGhoFlashMinter

Defines the behavior of the [GHOFlashMinter](../GhoFlashMinter).

The `IGhoFlashMinter` interface inherits the [`IERC3156FlashLender`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/interfaces/IERC3156FlashLender.sol) and [`IGhoFacilitator`](../../GHO/interfaces/IGhoFacilitator.md) interfaces.

This page shows the [events](#events), [write](#write-methods) and [view](#view-methods) methods within the `IGhoFlashMinter` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/flashMinter/interfaces/IGhoFlashMinter.sol).

## Events

### FeeUpdated

```solidity
event FeeUpdated(uint256 oldFee, uint256 newFee)
```

Emitted when the percentage [fee is updated](../GhoFlashMinter#updatefee).

| Name   | Type     | Description          |
| ------ | -------- | -------------------- |
| oldFee | `uint256 | The old fee (in bps) |
| newFee | `uint256 | The new fee (in bps) |

### FlashMint

```solidity
event FlashMint(
    address indexed receiver,
    address indexed initiator,
    address asset,
    uint256 indexed amount,
    uint256 fee
)
```

Emitted when a [FlashMint](../GhoFlashMinter.md#flashloan) occurs.

| Name      | Type      | Description                                                                      |
| --------- | --------- | -------------------------------------------------------------------------------- |
| receiver  | `address` | The receiver of the FlashMinted tokens (it is also the receiver of the callback) |
| initiator | `address` | The address initiating the FlashMint                                             |
| asset     | `address` | The asset being FlashMinted. Always GHO                                          |
| amount    | `uint256` | The principal being FlashMinted                                                  |
| fee       | `uint256` | The fee returned on top of the principal                                         |

## Write Methods

### updateFee

```solidity
function updateFee(uint256 newFee) external
```

Updates the percentage fee. It is the percentage of the flash-minted amount that needs to be repaid. The fee is expressed in bps. A value of 100, results in 1.00%

#### Input Parameters:

| Name   | Type      | Description                     |
| ------ | --------- | ------------------------------- |
| newFee | `uint256` | The new percentage fee (in bps) |

## View Methods

### ADDRESSES_PROVIDER

```solidity
function ADDRESSES_PROVIDER() external view returns (IPoolAddressesProvider)
```

Returns the address of the Aave Pool Addresses Provider contract.

#### Return Values:

| Type                     | Description                              |
| ------------------------ | ---------------------------------------- |
| `IPoolAddressesProvider` | The address of the PoolAddressesProvider |

### MAX_FEE

```solidity
function MAX_FEE() external view returns (uint256)
```

Returns the maximum value the fee can be set to.

#### Return Values:

| Type      | Description                                                                                    |
| --------- | ---------------------------------------------------------------------------------------------- |
| `uint256` | The maximum percentage fee of the flash-minted amount that the flashFee can be set to (in bps) |

### getFee

```solidity
function getFee() external view returns (uint256)
```

Returns the percentage of each flash mint taken as a fee.

#### Return Values:

| Type      | Description                                                                                             |
| --------- | ------------------------------------------------------------------------------------------------------- |
| `uint256` | The percentage fee of the flash-minted amount that needs to be repaid, on top of the principal (in bps) |

----
docs/developer-docs/aave-facilitator/GhoVariableDebtToken.md
# GhoVariableDebtToken

Implements a variable debt token to track the borrowing positions of users at variable rate mode for GHO.

:::info
It is important to note, although it is based on the VariableDebtToken implementation of the Aave Protocol, the interest rate mode is not variable as it is fixed by the Aave Governance.
:::

:::caution
A number of [operations](#not-supported-methods), such as transfer and approve, are disabled since it is a non-transferable token.
:::

The `GhoVariableDebtToken` contract inherits the [`DebtTokenBase`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/tokenization/base/DebtTokenBase.sol), [`ScaledBalanceTokenBase`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/tokenization/base/ScaledBalanceTokenBase.sol) contracts, and the [`IGhoVariableDebtToken`](./interfaces/IGhoVariableDebtToken.md) interface.

This page shows the public [constant state variables](#constant-state-variables), [structs](#structs), external [write](#write-methods) methods, and the ['not supported methods'](#not-supported-methods) within the `GhoVariableDebtToken` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/tokens/GhoVariableDebtToken.sol).

## Constant State Variables

### DEBT_TOKEN_REVISION

```solidity
uint256 public constant DEBT_TOKEN_REVISION = 0x1
```

The revision number of the contract.

## Structs

### GhoUserState

```solidity
struct GhoUserState {
    uint128 accumulatedDebtInterest;
    uint16 discountPercent;
    uint40 rebalanceTimestamp;
}
```

| Name                    | Type      | Description                                              |
| ----------------------- | --------- | -------------------------------------------------------- |
| accumulatedDebtInterest | `uint128` | The accumulated debt interest of the user                |
| discountPercent         | `uint16`  | The discount percent of the user (expressed in bps)      |
| rebalanceTimestamp      | `uint40`  | The timestamp when the user’s discount can be rebalanced |

## Write Methods

### initialize

```solidity
function initialize(
    IPool initializingPool,
    address underlyingAsset,
    IAaveIncentivesController incentivesController,
    uint8 debtTokenDecimals,
    string memory debtTokenName,
    string memory debtTokenSymbol,
    bytes calldata params
  ) external override initializer
```

Initializes the debt token.

Emits the [`Initialized`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IInitializableDebtToken.sol#L23) event.

#### Input Parameters:

| Name                 | Type                        | Description                                                   |
| -------------------- | --------------------------- | ------------------------------------------------------------- |
| initializingPool     | `IPool`                     | The pool contract that is initializing this contract          |
| underlyingAsset      | `address`                   | The address of the underlying asset of this aToken            |
| incentivesController | `IAaveIncentivesController` | The smart contract managing potential incentives distribution |
| debtTokenDecimals    | `uint8`                     | The decimals of the debtToken, same as the underlying asset’s |
| debtTokenName        | `string`                    | The name of the token                                         |
| debtTokenSymbol      | `string`                    | The symbol of the token                                       |
| params               | `bytes`                     | A set of encoded parameters for additional initialization     |

### mint

```solidity
function mint(
    address user,
    address onBehalfOf,
    uint256 amount,
    uint256 index
) external virtual override onlyPool returns (bool, uint256)
```

- Mints the debt token to the `onBehalfOf` address. Implements the basic logic to mint a scaled balance token.
- The user’s interest is accumulated here.
- The discount percent of the user is applied to the accumulated interest.
- DiscountPercent is rebalanced and “locked for the next period of time”

#### Input Parameters:

| Name       | Type       | Description                                                                                                                                                      |
| ---------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| user       | `address` | The address performing the mint. The address receives the borrowed underlying, being the delegatee in case of credit delegation, or same as onBehalfOf otherwise |
| onBehalfOf | `address`  | The address of the user that will receive the scaled debt tokens tokens                                                                                          |
| amount     | `uint256`  | The amount of debt tokens being minted                                                                                                                           |
| index      | `uint256`  | The next variable debt liquidity index of the reserve                                                                                                            |

#### Return Values:

| Type      | Description                                                        |
| --------- | ------------------------------------------------------------------ |
| `bool`    | true if the the previous balance of the user is 0, false otherwise |
| `uint256` | The scaled total debt of the reserve                               |

### burn

```solidity
function burn(
    address from,
    uint256 amount,
    uint256 index
) external override onlyPool returns (uint256)
```

Burns the user variable debt token. Implements the basic logic to burn a scaled balance token.

#### Input Parameters:

| Name   | Type      | Description                                    |
| ------ | --------- | ---------------------------------------------- |
| from   | `address` | The address from which the debt will be burned |
| amount | `uint256` | The amount being burned                        |
| index  | `uint256` | The variable debt index of the reserve         |

#### Return Values:

| Type      | Description                          |
| --------- | ------------------------------------ |
| `uint256` | The scaled total debt of the reserve |

### setAToken

```solidity
function setAToken(address ghoAToken) external override onlyPoolAdmin
```

Sets a reference to the [`GhoAToken`](GhoAToken.md) contract. Checks the AToken has not already been set.

This function can only be called by the [Pool Admin](../contracts-overview.md#accounts-after-deployment).

Emits the [`ATokenSet`](./interfaces/IGhoVariableDebtToken#atokenset) event.

#### Input Parameters:

| Name      | Type      | Description                           |
| --------- | --------- | ------------------------------------- |
| ghoAToken | `address` | The address of the GhoAToken contract |

### updateDiscountRateStrategy

```solidity
function updateDiscountRateStrategy(address newDiscountRateStrategy)
    external
    override
    onlyPoolAdmin
```

Updates the Discount Rate Strategy.

This function can only be called by the [Pool Admin](../contracts-overview.md#accounts-after-deployment).

Emits the [`DiscountRateStrategyUpdated`](./interfaces/IGhoVariableDebtToken.md#discountratestrategyupdated) event.

#### Input Parameters:

| Name                    | Type      | Description                                      |
| ----------------------- | --------- | ------------------------------------------------ |
| newDiscountRateStrategy | `address` | The address of the DiscountRateStrategy contract |

### updateDiscountToken

```solidity
function updateDiscountToken(address newDiscountToken) external override onlyPoolAdmin
```

Updates the Discount Token.

This function can only be called by the [Pool Admin](../contracts-overview.md#accounts-after-deployment).

Emits the [`DiscountTokenUpdated`](./interfaces/IGhoVariableDebtToken.md#discounttokenupdated) event.

#### Input Parameters:

| Name             | Type      | Description                           |
| ---------------- | --------- | ------------------------------------- |
| newDiscountToken | `address` | The address of DiscountToken contract |

### updateDiscountDistribution

```solidity
function updateDiscountDistribution(
    address sender,
    address recipient,
    uint256 senderDiscountTokenBalance,
    uint256 recipientDiscountTokenBalance,
    uint256 amount
  ) external override onlyDiscountToken
```

Updates the discount percents of the users when a discount token transfer occurs.

This function is automatically called when `stkAAVE` tokens are transferred into the user’s address.

This function can only be called by the discount token.

Emits the [`Transfer`](https://github.com/aave/aave-v3-core/blob/master/contracts/dependencies/openzeppelin/contracts/IERC20.sol#L73) and [`Mint`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IScaledBalanceToken.sol#L18) events.

#### Input Parameters:

| Name                          | Type      | Description                                    |
| ----------------------------- | --------- | ---------------------------------------------- |
| sender                        | `address` | The address of the sender                      |
| recipient                     | `address` | The address of the recipient                   |
| senderDiscountTokenBalance    | `uint256` | The sender discount token balance              |
| recipientDiscountTokenBalance | `uint256` | The recipient discount token balance           |
| amount                        | `uint256` | The amount of discount token being transferred |

### decreaseBalanceFromInterest

```solidity
function decreaseBalanceFromInterest(address user, uint256 amount) external override onlyAToken
```

Decreases the amount of interest accumulated by the user.

This function can only be called by the AToken.

#### Input Parameters:

| Name   | Type      | Description               |
| ------ | --------- | ------------------------- |
| user   | `address` | The address of the user   |
| amount | `uint256` | The value to be decreased |

### rebalanceUserDiscountPercent

```solidity
function rebalanceUserDiscountPercent(address user) external override
```

Rebalances the discount percent of a user.

This can only be called if the the discount lock period has finished and the user has a discount rate to be rebalanced.

Emits the [`Transfer`](https://github.com/aave/aave-v3-core/blob/master/contracts/dependencies/openzeppelin/contracts/IERC20.sol#L73) and [`Mint`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IScaledBalanceToken.sol#L18) events.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

### updateDiscountLockPeriod

```solidity
function updateDiscountLockPeriod(uint256 newLockPeriod) external override onlyPoolAdmin
```

Updates the discount percent lock period.

This function can only be called by the [Pool Admin](../contracts-overview.md#accounts-after-deployment).

Emits the [`DiscountLockPeriodUpdated`](./interfaces/IGhoVariableDebtToken.md#discountlockperiodupdated) event.

#### Input Parameters:

| Name          | Type      | Description                                       |
| ------------- | --------- | ------------------------------------------------- |
| newLockPeriod | `uint256` | The new discount percent lock period (in seconds) |

## View Methods

### balanceOf

```solidity
function balanceOf(address user) public view virtual override returns (uint256)
```

Returns the amount of tokens owned by the `user`.

Standard [`ERC20`](https://github.com/aave/aave-v3-core/blob/master/contracts/dependencies/openzeppelin/contracts/IERC20.sol#L16) method.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

#### Return Values:

| Type      | Description                            |
| --------- | -------------------------------------- |
| `uint256` | The amount of tokens owned by the user |

### totalSupply

```solidity
function totalSupply() public view virtual override returns (uint256)
```

Returns the amount of tokens in existence.

It does not account for active discounts of the users. The discount is deducted from the user’s debt at repayment / liquidation time, so this function always return a greater or equal value than the actual total supply.

Standard [`ERC20`](https://github.com/aave/aave-v3-core/blob/master/contracts/dependencies/openzeppelin/contracts/IERC20.sol#L11) method.

#### Return Values:

| Type      | Description                                                                         |
| --------- | ----------------------------------------------------------------------------------- |
| `uint256` | The amount of tokens in existence (without accounting for active discounts on debt) |

### UNDERLYING_ASSET_ADDRESS

```solidity
function UNDERLYING_ASSET_ADDRESS() external view override returns (address)
```

Returns the address of the underlying asset of this debtToken, GHO for variableDebtGHO.

#### Return Values:

| Type      | Description                         |
| --------- | ----------------------------------- |
| `address` | The address of the underlying asset |

### getAToken

```solidity
function getAToken() external view override returns (address)
```

Returns the address of the [`GhoAToken`](GhoAToken.md) contract.

#### Return Values:

| Type      | Description                           |
| --------- | ------------------------------------- |
| `address` | The address of the GhoAToken contract |

### getDiscountRateStrategy

```solidity
function getDiscountRateStrategy() external view override returns (address)
```

Returns the address of the Discount Rate Strategy.

#### Return Values:

| Type      | Description                                      |
| --------- | ------------------------------------------------ |
| `address` | The address of the DiscountRateStrategy contract |

### getDiscountToken

```solidity
function getDiscountToken() external view override returns (address)
```

Returns the address of the Discount Token.

#### Return Values:

| Type      | Description                   |
| --------- | ----------------------------- |
| `address` | The address of Discount Token |

### getDiscountPercent

```solidity
function getDiscountPercent(address user) external view override returns (uint256)
```

Returns the discount percent that will be applied to the accumulated borrow interest of the user.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

#### Return Values:

| Type      | Description                             |
| --------- | --------------------------------------- |
| `uint256` | The discount percent (expressed in bps) |

### getBalanceFromInterest

```solidity
function getBalanceFromInterest(address user) external view override returns (uint256)
```

Returns the amount of interest accumulated by the user.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

#### Return Values:

| Type      | Description                                    |
| --------- | ---------------------------------------------- |
| `uint256` | The amount of interest accumulated by the user |

### getDiscountLockPeriod

```solidity
function getDiscountLockPeriod() external view override returns (uint256)
```

Returns the discount percent lock period.

#### Return Values:

| Type      | Description                                   |
| --------- | --------------------------------------------- |
| `uint256` | The discount percent lock period (in seconds) |

### getUserRebalanceTimestamp

```solidity
function getUserRebalanceTimestamp(address user) external view override returns (uint256)
```

Returns the timestamp at which a user’s discount percent can be rebalanced.

#### Input Parameters:

| Name | Type      | Description                                                   |
| ---- | --------- | ------------------------------------------------------------- |
| user | `address` | The address of the user’s rebalance timestamp being requested |

#### Return Values:

| Type      | Description                                               |
| --------- | --------------------------------------------------------- |
| `uint256` | The time when a user’s discount percent can be rebalanced |

## NOT SUPPORTED METHODS

The following methods automatically revert with the error code `80`. The methods show `OPERATION_NOT_SUPPORTED` as they are not permitted to be executed.

Being non-transferrable, the debt token does not implement any of the standard ERC20 functions for transfer and allowance.

### transfer

```solidity
function transfer(address, uint256) external virtual override returns (bool)
```

:::danger Not supported by design.
:::

### allowance

```solidity
function allowance(address, address) external view virtual override returns (uint256)
```

:::danger Not supported by design.
:::

### approve

```solidity
function approve(address, uint256) external virtual override returns (bool)
```

:::danger Not supported by design.
:::

### transferFrom

```solidity
function transferFrom(
    address,
    address,
    uint256
) external virtual override returns (bool)
```

:::danger Not supported by design.
:::

### increaseAllowance

```solidity
function increaseAllowance(address, uint256) external virtual override returns (bool)
```

:::danger Not supported by design.
:::

### decreaseAllowance

```solidity
function decreaseAllowance(address, uint256) external virtual override returns (bool)
```

:::danger Not supported by design.
:::

----
docs/developer-docs/aave-facilitator/_category_.json
{
  "label": "Aave Facilitator",
  "position": 3,
  "link": {
    "type": "generated-index"
  }
}

----
docs/developer-docs/aave-facilitator/GhoInterestRateStrategy.md
# GhoInterestRateStrategy

This contract implements the calculation of the GHO interest rates.

The variable borrow interest rate is fixed at deployment time. The Aave Governance can update the interest rate by deploying a brand new contract and injecting it to the GHO reserve.

The `GhoInterestRateStrategy` contract inherits the [`IReserveInterestRateStrategy`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IReserveInterestRateStrategy.sol) interface.

This page shows the external [view](#view-methods) methods within the `GhoInterestRateStrategy` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/interestStrategy/GhoInterestRateStrategy.sol).

## View Methods

### calculateInterestRates

```solidity
function calculateInterestRates(DataTypes.CalculateInterestRatesParams memory params)
    public
    view
    override
    returns (
      uint256,
      uint256,
      uint256
    )
```

Calculates the interest rates depending on the reserve’s state and configurations.

:::info

As the variable rate is fixed for the current interest rate strategy, parameters are not used for the interest rate calculation. No matter what the parameters are, the `liquidityRate` and `stableRate` will be 0. The interest rate returned, `variableBorrowRate`, is the fixed value decided by Aave Governance.

:::

#### Input Parameters:

| Name     | Type                                                                                                   | Description                                       |
| -------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------- |
| CalculateInterestRatesParams | [`params`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/libraries/types/DataTypes.sol#L247) | The parameters needed to calculate interest rates |

#### Return Values:

| Name               | Type    | Description                                                                                            |
| ------------------ | ------- | ------------------------------------------------------------------------------------------------------ |
| liquidityRate      | `uint256` | The liquidity rate = 0                                                                                 |
| stableBorrowRate   | `uint256` | The stable borrow rate = 0                                                                             |
| variableBorrowRate | `uint256` | The variable borrow rate decided by Aave Governance, expressed in ray (27 decimal fixed point number). |

----
docs/developer-docs/aave-facilitator/GhoDiscountRateStrategy.md
# GhoDiscountRateStrategy

This contract implements the calculation of the discount rate depending on the current strategy.

The `GhoDiscountRateStrategy` contract inherits the [`IGhoDiscountRateStrategy`](./interfaces/IGhoDiscountRateStrategy) interface.

This page shows the public [constant state variables](#constant-state-variables), and external [pure methods](#pure-methods) within the `GhoDiscountRateStrategy` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/interestStrategy/GhoDiscountRateStrategy.sol).

<aside>

:::tip **Debt and Discount Token**

Debt Token = GHO, the discounted token
Discount Token = stkAAVE, per the initial design OR current configuration
:::

</aside>

## Constant State Variables

### GHO_DISCOUNTED_PER_DISCOUNT_TOKEN

```solidity
uint256 public constant GHO_DISCOUNTED_PER_DISCOUNT_TOKEN = 100e18
```

The amount of debt that is entitled to get a discount per unit of discount token (stkAAVE).

Expressed with the number of decimals of the discounted token (GHO).

### DISCOUNT_RATE

```solidity
uint256 public constant DISCOUNT_RATE = 2000
```

The percentage of discount to apply to the part of the debt that is entitled to get a discount.

Expressed in bps. For example, a value of 2000 results in 20.00%.

### MIN_DISCOUNT_TOKEN_BALANCE

```solidity
uint256 public constant MIN_DISCOUNT_TOKEN_BALANCE = 1e18
```

The minimum balance amount of discount token (stkAAVE) a user must hold to be entitled to a discount.

Expressed with the number of decimals of the discount token (stkAAVE).

### MIN_DEBT_TOKEN_BALANCE

```solidity
uint256 public constant MIN_DEBT_TOKEN_BALANCE = 1e18
```

Minimum balance amount of debt token (variableEthDebtGHO) to be entitled to a discount.

Expressed with the number of decimals of the debt token (GHO).

## Pure Methods

### calculateDiscountRate

```solidity
function calculateDiscountRate(uint256 debtBalance, uint256 discountTokenBalance)
    external
    pure
    override
    returns (uint256)
```

Calculates the discount rate depending on the debt token (GHO) and discount token (stkAAVE) balances.

The `debtBalance` and `discountTokenBalance` must be above the [`MIN_DEBT_TOKEN_BALANCE`](#mindebttokenbalance) and [`MIN_DISCOUNT_TOKEN_BALANCE`](#mindiscounttokenbalance)` respectively, to receive a discount.

Please see the [Discount Rate](../../concepts/fundamental-concepts/gho-discount-strategy) page for more information and examples of the discount rate implementation.

#### Input Parameters:

| Name                 | Type      | Description                                      |
| -------------------- | --------- | ------------------------------------------------ |
| debtBalance          | `uint256` | The debt balance of the user                     |
| discountTokenBalance | `uint256` | The discount token (stkAAVE) balance of the user |

#### Return Values:

| Type      | Description                                                                |
| --------- | -------------------------------------------------------------------------- |
| `uint256` | The discount rate, as a percentage - the maximum can be 10000bps = 100.00% |

----
docs/developer-docs/aave-facilitator/GhoAToken.md
# GhoAToken

The implementation of the interest bearing token for the Aave Protocol.

:::info

GHO cannot be supplied to the Aave Protocol. However, the `GhoAToken` is required as it contains logic for GHO to work as a reserve with the Aave Protocol.

:::

The `GhoAToken` contract inherits the [`VersionedInitializable`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/libraries/aave-upgradeability/VersionedInitializable.sol), [`ScaledBalanceTokenBase`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/tokenization/base/ScaledBalanceTokenBase.sol) and [`EIP712Base`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/tokenization/base/EIP712Base.sol) contracts, and the [`IGhoAToken`](./interfaces/IGhoAToken.md) interface.

This page shows the public [constant state variables](#constant-state-variables), external [write](#write-methods) and [view](#view-methods) methods, and the ['not permitted methods'](#not-permitted-methods) within the `GhoAToken` contract. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/tokens/GhoAToken.sol).

## Constant State Variables

The external state variables.

### PERMIT_TYPEHASH

```solidity
bytes32 public constant PERMIT_TYPEHASH =
    keccak256('Permit(address owner,address spender,uint256 value,uint256 nonce,uint256 deadline)')
```

### ATOKEN_REVISION

```solidity
uint256 public constant ATOKEN_REVISION = 0x1
```

## Write Methods

### initialize

```solidity
function initialize(
    IPool initializingPool,
    address treasury,
    address underlyingAsset,
    IAaveIncentivesController incentivesController,
    uint8 aTokenDecimals,
    string calldata aTokenName,
    string calldata aTokenSymbol,
    bytes calldata params
  ) external override initializer
```

Initializes the `aToken`.

Emits the [`Initialized`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IInitializableAToken.sol#L24) event.

#### Input Parameters:

| Name                 | Type                        | Description                                                         |
| -------------------- | --------------------------- | ------------------------------------------------------------------- |
| initializingPool     | `IPool`                     | The pool contract that is initializing this contract                |
| treasury             | `address`                   | The address of the Aave treasury, receiving the fees on this aToken |
| underlyingAsset      | `address`                   | The address of the underlying asset of this aToken, GHO             |
| incentivesController | `IAaveIncentivesController` | The smart contract managing potential incentives distribution       |
| aTokenDecimals       | `uint8`                     | The decimals of the aToken, same as the underlying asset’s, 18      |
| aTokenName           | `string`                    | The name of the aToken, ghoAToken                                   |
| aTokenSymbol         | `string`                    | The symbol of the aToken, GHO                                       |
| params               | `bytes`                     | A set of encoded parameters for additional initialization           |

### transferUnderlyingTo

```solidity
function transferUnderlyingTo(address target, uint256 amount) external virtual override onlyPool
```

Transfers the underlying asset to `target`.

It performs a mint of GHO on behalf of the `target`. Used by the Pool to transfer assets in `borrow()`.

#### Input Parameters:

| Name   | Type      | Description                           |
| ------ | --------- | ------------------------------------- |
| target | `address` | The recipient of the underlying token |
| amount | `uint256` | The amount getting transferred        |

### handleRepayment

```solidity
function handleRepayment(
    address user,
    address onBehalfOf,
    uint256 amount
) external virtual override onlyPool
```

Handles the underlying received by the aToken after the transfer has been completed.

This function transfers the debt interest repaid by a user to the GHO treasury. It burns all the repaid GHO.

#### Input Parameters:

| Name       | Type      | Description                                                      |
| ---------- | --------- | ---------------------------------------------------------------- |
| user       | `address` | The user executing the repayment                                 |
| onBehalfOf | `address` | The address of the user who will get their debt reduced/removed. |
| amount     | `uint256` | The amount getting repaid                                        |

### distributeFeesToTreasury

```solidity
function distributeFeesToTreasury() external virtual override
```

Distribute accumulated fees to the GHO treasury.

Emits the [`FeesDistributedToTreasury`](../GHO/interfaces/IGhoFacilitator#feesdistributedtotreasury) event.

### rescueTokens

```solidity
function rescueTokens(
    address token,
    address to,
    uint256 amount
) external override onlyPoolAdmin
```

Rescues and transfers the tokens locked in this contract to the recipient.

The underlying asset, GHO, cannot be rescued.

#### Input Parameters:

| Name   | Type      | Description                     |
| ------ | --------- | ------------------------------- |
| token  | `address` | The address of the token        |
| to     | `address` | The address of the recipient    |
| amount | `uint256` | The amount of token to transfer |

### setVariableDebtToken

```solidity
function setVariableDebtToken(address ghoVariableDebtToken) external override onlyPoolAdmin
```

Sets a reference to the GHO variable debt token. The variable debt token must not already be set.

Emits the [`VariableDebtTokenSet`](./interfaces/IGhoAToken.md#variabledebttokenset) event.

#### Input Parameters:

| Name                 | Type       | Description                               |
| -------------------- | ---------- | ----------------------------------------- |
| ghoVariableDebtToken | `address ` | The address of the `GHOVariableDebtToken` |

### updateGhoTreasury

```solidity
function updateGhoTreasury(address newGhoTreasury) external override onlyPoolAdmin
```

Updates the address of the GHO treasury, where interest earned by the protocol is sent.

Emits the [`GhoTreasuryUpdated`](../GHO/interfaces/IGhoFacilitator.md#ghotreasuryupdated) event.

#### Input Parameters:

| Name           | Type      | Description                    |
| -------------- | --------- | ------------------------------ |
| newGhoTreasury | `address` | The address of the GhoTreasury |

## View Methods

The [`balanceOf`](#balanceof) and [`totalSupply`](#totalsupply) methods, both return zero. The reason is that GHO cannot be supplied to the Aave Protocol. However, the `GhoAToken` is required as it contains logic for GHO to work as a reserve with the Aave Protocol.

### balanceOf

```solidity
function balanceOf(address user)
    public
    view
    virtual
    override(IncentivizedERC20, IERC20)
    returns (uint256)
```

Returns zero at `GhoAToken`.

Standard [`ERC20`](https://github.com/aave/aave-v3-core/blob/master/contracts/dependencies/openzeppelin/contracts/IERC20.sol#L16) method.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

#### Return Values:

| Type      | Description |
| --------- | ----------- |
| `uint256` | 0           |

### totalSupply

```solidity
function totalSupply() public view virtual override(IncentivizedERC20, IERC20) returns (uint256)
```

Returns zero at `GhoAToken`.

Standard [`ERC20`](https://github.com/aave/aave-v3-core/blob/master/contracts/dependencies/openzeppelin/contracts/IERC20.sol#L11) method.

#### Return Values:

| Type      | Description |
| --------- | ----------- |
| `uint256` | 0           |

### RESERVE_TREASURY_ADDRESS

```solidity
function RESERVE_TREASURY_ADDRESS() external view override returns (address)
```

Returns the `address` of the Aave treasury.

#### Return Values:

| Type      | Description                      |
| --------- | -------------------------------- |
| `address` | The address of the Aave treasury |

### UNDERLYING_ASSET_ADDRESS

```solidity
function UNDERLYING_ASSET_ADDRESS() external view override returns (address)
```

Returns the `address` of GHO as it is the underlying asset of this aToken.

#### Return Values:

| Type      | Description                              |
| --------- | ---------------------------------------- |
| `address` | The address of the underlying asset, GHO |

### DOMAIN_SEPARATOR

```solidity
function DOMAIN_SEPARATOR() public view override(IAToken, EIP712Base) returns (bytes32)
```

Overrides the base function to fully implement [`IAToken`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IAToken.sol).

Gets the domain separator for the token. Return cached value if chainId matches cache, otherwise recomputes separator.

See [`EIP712Base.DOMAIN_SEPARATOR()`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/tokenization/base/EIP712Base.sol#L32) for more detailed documentation.

#### Return Values:

| Type      | Description                                            |
| --------- | ------------------------------------------------------ |
| `bytes32` | The domain separator of the token on the current chain |

### nonces

```solidity
function nonces(address owner) public view override(IAToken, EIP712Base) returns (uint256)
```

Overrides the base function to fully implement [`IAToken`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IAToken.sol).

Returns the nonce of the `owner`.

See [`EIP712Base.nonces()`](https://github.com/aave/aave-v3-core/blob/master/contracts/protocol/tokenization/base/EIP712Base.sol#L44) for more detailed documentation.

#### Input Parameters:

| Name  | Type      | Description              |
| ----- | --------- | ------------------------ |
| owner | `address` | The address of the owner |

#### Return Values:

| Type      | Description            |
| --------- | ---------------------- |
| `uint256` | The nonce of the owner |

### getVariableDebtToken

```solidity
function getVariableDebtToken() external view override returns (address)
```

Returns the `address` of the GHO variable debt token.

#### Return Values:

| Type      | Description                                        |
| --------- | -------------------------------------------------- |
| `address` | The address of the `GhoVariableDebtToken` contract |

### getGhoTreasury

```solidity
function getGhoTreasury() external view override returns (address) {
```

Returns the `address` of the GHO treasury.

#### Return Values:

| Type      | Description                             |
| --------- | --------------------------------------- |
| `address` | The address of the GhoTreasury contract |

## NOT PERMITTED METHODS

The following methods automatically revert with the error from Aave V3 `OPERATION_NOT_SUPPORTED` as they are not permitted to be executed.

For example, [`mint()`](#mint) is not permitted as it is not possible to supply GHO into the pool.

### mint

```solidity
function mint(
    address caller,
    address onBehalfOf,
    uint256 amount,
    uint256 index
) external virtual override onlyPool returns (bool)
```

Not permitted by design.

### burn

```solidity
function burn(
    address from,
    address receiverOfUnderlying,
    uint256 amount,
    uint256 index
  ) external virtual override onlyPool
```

Not permitted by design.

### mintToTreasury

```solidity
function mintToTreasury(uint256 amount, uint256 index) external virtual override onlyPool
```

Not permitted by design.

### transferOnLiquidation

```solidity
function transferOnLiquidation(
    address from,
    address to,
    uint256 value
) external virtual override onlyPool
```

Not permitted by design.

### permit

```solidity
function permit(
    address owner,
    address spender,
    uint256 value,
    uint256 deadline,
    uint8 v,
    bytes32 r,
    bytes32 s
) external
```

Not permitted by design.

----
docs/developer-docs/aave-facilitator/interfaces/IGhoAToken.md
# IGhoAToken

Defines the basic interface of the [`GhoAToken`](../GhoAToken.md).

The `IGhoAToken` interface inherits the [`IAToken`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IAToken.sol) and [`IGhoFacilitator`](../../GHO/interfaces/IGhoFacilitator) interface.

This page shows the [events](#events), [write](#write-methods) and [view](#view-methods) methods within the `IGhoAToken` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/tokens/interfaces/IGhoAToken.sol).

## Events

### VariableDebtTokenSet

```solidity
event VariableDebtTokenSet(address indexed variableDebtToken)
```

Emitted when a reference to the GHO [variable debt token is set](../GhoAToken.md#setvariabledebttoken).

#### Input Parameters:

| Name              | Type      | Description                                        |
| ----------------- | --------- | -------------------------------------------------- |
| variableDebtToken | `address` | The address of the `GhoVariableDebtToken` contract |

## Write Methods

### setVariableDebtToken

```solidity
function setVariableDebtToken(address GhoVariableDebtToken) external
```

Sets a reference to the GHO variable debt token.

#### Input Parameters:

| Name                 | Type      | Description                                        |
| -------------------- | --------- | -------------------------------------------------- |
| GhoVariableDebtToken | `address` | The address of the `GhoVariableDebtToken` contract |

## View Methods

### getVariableDebtToken

```solidity
function getVariableDebtToken() external view returns (address)
```

Returns the `address` of the GHO variable debt token.

#### Return Values:

| Type      | Description                                        |
| --------- | -------------------------------------------------- |
| `address` | The address of the `GhoVariableDebtToken` contract |

----
docs/developer-docs/aave-facilitator/interfaces/_category_.json
{
  "label": "Interfaces",
  "link": {
    "type": "generated-index"
  }
}
----
docs/developer-docs/aave-facilitator/interfaces/IGhoVariableDebtToken.md
# IGhoVariableDebtToken

Defines the basic interface of the [`GhoVariableDebtToken`](../GhoVariableDebtToken).

The `IGhoVariableDebtToken` interface inherits the [`IVariableDebtToken`](https://github.com/aave/aave-v3-core/blob/master/contracts/interfaces/IVariableDebtToken.sol) interface.

This page shows the [events](#events), [write](#write-methods) and [view](#view-methods) methods within the `IGhoVariableDebtToken` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/tokens/interfaces/IGhoVariableDebtToken.sol).

## Events

### ATokenSet

```solidity
event ATokenSet(address indexed aToken)
```

Emitted when the address of the GHO [`aToken is set`](../GhoVariableDebtToken#setatoken).

#### Input Parameters:

| Name   | Type      | Description                             |
| ------ | --------- | --------------------------------------- |
| aToken | `address` | The address of the `GhoAToken` contract |

### DiscountRateStrategyUpdated

```solidity
event DiscountRateStrategyUpdated(
    address indexed oldDiscountRateStrategy,
    address indexed newDiscountRateStrategy
)
```

Emitted when the [discount rate strategy is updated](../GhoVariableDebtToken#updatediscountratestrategy).

#### Input Parameters:

| Name                    | Type      | Description                                    |
| ----------------------- | --------- | ---------------------------------------------- |
| oldDiscountRateStrategy | `address` | The address of the old GhoDiscountRateStrategy |
| newDiscountRateStrategy | `address` | The address of the new GhoDiscountRateStrategy |

### DiscountTokenUpdated

```solidity
event DiscountTokenUpdated(address indexed oldDiscountToken, address indexed newDiscountToken)
```

Emitted when the [discount token is updated](../GhoVariableDebtToken#updatediscounttoken).

#### Input Parameters:

| Name             | Type      | Description                           |
| ---------------- | --------- | ------------------------------------- |
| oldDiscountToken | `address` | The address of the old discount token |
| newDiscountToken | `address` | The address of the new discount token |

### DiscountLockPeriodUpdated

```solidity
event DiscountLockPeriodUpdated(
    uint256 indexed oldDiscountLockPeriod,
    uint256 indexed newDiscountLockPeriod
)
```

Emitted when the [discount lock period is updated](../GhoVariableDebtToken#updatediscountlockperiod).

#### Input Parameters:

| Name                  | Type      | Description                             |
| --------------------- | --------- | --------------------------------------- |
| oldDiscountLockPeriod | `uint256` | The value of the old DiscountLockPeriod |
| newDiscountLockPeriod | `uint256` | The value of the new DiscountLockPeriod |

### DiscountPercentLocked

```solidity
event DiscountPercentLocked(
    address indexed user,
    uint256 oldDiscountPercent,
    uint256 indexed newDiscountPercent,
    uint256 indexed rebalanceTimestamp
)
```

Emitted when the internal function [`_refreshDiscountPercent`](https://github.com/aave/gho/blob/main/src/contracts/facilitators/aave/tokens/GhoVariableDebtToken.sol#L522) is called, which updates the discount percent of the user according to current discount rate strategy.

#### Input Parameters:

| Name               | Type      | Description                                                   |
| ------------------ | --------- | ------------------------------------------------------------- |
| user               | `address` | The address of the user                                       |
| oldDiscountPercent | `uint256` | The old discount percent of the user                          |
| newDiscountPercent | `uint256` | The new discount percent of the user                          |
| rebalanceTimestamp | `uint256` | The Timestamp when a user’s locked discount can be rebalanced |

## Write Methods

### setAToken

```solidity
function setAToken(address ghoAToken) external
```

Sets a reference to the GHO aToken.

#### Input Parameters:

| Name      | Type      | Description                           |
| --------- | --------- | ------------------------------------- |
| ghoAToken | `address` | The address of the GhoAToken contract |

### updateDiscountRateStrategy

```solidity
function updateDiscountRateStrategy(address newDiscountRateStrategy) external
```

Updates the Discount Rate Strategy.

#### Input Parameters:

| Name                    | Type      | Description                                     |
| ----------------------- | --------- | ----------------------------------------------- |
| newDiscountRateStrategy | `address` | The address of GhoDiscountRateStrategy contract |

### updateDiscountToken

```solidity
function updateDiscountToken(address newDiscountToken) external
```

Updates the Discount Token.

#### Input Parameters:

| Name             | Type      | Description                           |
| ---------------- | --------- | ------------------------------------- |
| newDiscountToken | `address` | The address of DiscountToken contract |

### updateDiscountDistribution

```solidity
function updateDiscountDistribution(
    address sender,
    address recipient,
    uint256 senderDiscountTokenBalance,
    uint256 recipientDiscountTokenBalance,
    uint256 amount
) external
```

Updates the discount percents of the users when a discount token transfer occurs.

#### Input Parameters:

| Name                          | Type      | Description                                    |
| ----------------------------- | --------- | ---------------------------------------------- |
| sender                        | `address` | The address of the sender                      |
| recipient                     | `address` | The address of the recipient                   |
| senderDiscountTokenBalance    | `uint256` | The sender discount token balance              |
| recipientDiscountTokenBalance | `uint256` | The recipient discount token balance           |
| amount                        | `uint256` | The amount of discount token being transferred |

### decreaseBalanceFromInterest

```solidity
function decreaseBalanceFromInterest(address user, uint256 amount) external
```

Decrease the `amount` of interests accumulated by the `user`.

#### Input Parameters:

| Name   | Type      | Description               |
| ------ | --------- | ------------------------- |
| user   | `address` | The address of the user   |
| amount | `uint256` | The value to be decreased |

### rebalanceUserDiscountPercent

```solidity
function rebalanceUserDiscountPercent(address user) external
```

Rebalances the discount percent of a `user` if they are past their rebalance timestamp.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

### updateDiscountLockPeriod

```solidity
function updateDiscountLockPeriod(uint256 newLockPeriod) external
```

Updates the discount percent lock period.

#### Input Parameters:

| Name          | Type      | Description                               |
| ------------- | --------- | ----------------------------------------- |
| newLockPeriod | `uint256` | The new discount lock period (in seconds) |

## View Methods

### getAToken

```solidity
function getAToken() external view returns (address)
```

Returns the `address` of the GHO aToken.

#### Return Values:

| Type      | Description                           |
| --------- | ------------------------------------- |
| `address` | The address of the GhoAToken contract |

### getDiscountRateStrategy

```solidity
function getDiscountRateStrategy() external view returns (address)
```

Returns the `address` of the Discount Rate Strategy.

#### Return Values:

| Type      | Description                                     |
| --------- | ----------------------------------------------- |
| `address` | The address of GhoDiscountRateStrategy contract |

### getDiscountToken

```solidity
function getDiscountToken() external view returns (address)
```

Returns the `address` of the Discount Token.

#### Return Values:

| Type      | Description                  |
| --------- | ---------------------------- |
| `address` | The address of DiscountToken |

### getDiscountPercent

```solidity
function getDiscountPercent(address user) external view returns (uint256)
```

Returns the discount percent being applied to the debt interest of the `user`.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

#### Return Values:

| Type      | Description                             |
| --------- | --------------------------------------- |
| `uint256` | The discount percent (expressed in bps) |

### getBalanceFromInterest

```solidity
function getBalanceFromInterest(address user) external view returns (uint256)
```

Returns the amount of interests accumulated by the `user`.

#### Input Parameters:

| Name | Type      | Description             |
| ---- | --------- | ----------------------- |
| user | `address` | The address of the user |

#### Return Values:

| Type      | Description                                     |
| --------- | ----------------------------------------------- |
| `uint256` | The amount of interests accumulated by the user |

### getDiscountLockPeriod

```solidity
function getDiscountLockPeriod() external view returns (uint256)
```

Returns the discount percent lock period.

#### Return Values:

| Type      | Description                                   |
| --------- | --------------------------------------------- |
| `uint256` | The discount percent lock period (in seconds) |

### getUserRebalanceTimestamp

```solidity
function getUserRebalanceTimestamp(address user) external view returns (uint256)
```

Returns the timestamp at which a discount percent can be rebalanced for a `user`.

#### Input Parameters:

| Name | Type      | Description                                                   |
| ---- | --------- | ------------------------------------------------------------- |
| user | `address` | The address of the user’s rebalance timestamp being requested |

#### Return Values:

| Type      | Description                                      |
| --------- | ------------------------------------------------ |
| `uint256` | The time when a users discount can be rebalanced |

----
docs/developer-docs/aave-facilitator/interfaces/IGhoDiscountRateStrategy.md
# IGhoDiscountRateStrategy

Defines the basic interface of the [`GhoDiscountRateStrategy`](../GhoDiscountRateStrategy).

This page shows the [view](#view-methods) methods within the `IGhoDiscountRateStrategy` interface. The source code is available on [GitHub](https://github.com/aave/gho-core/blob/main/src/contracts/facilitators/aave/tokens/interfaces/IGhoDiscountRateStrategy.sol).

## View Methods

### calculateDiscountRate

```solidity
function calculateDiscountRate(uint256 debtBalance, uint256 discountTokenBalance)
    external
    view
    returns (uint256)
```

Calculates the discount rate depending on the debt and discount token balances.

#### Input Parameters:

| Name                 | Type      | Description                            |
| -------------------- | --------- | -------------------------------------- |
| debtBalance          | `uint256` | The debt balance of the user           |
| discountTokenBalance | `uint256` | The discount token balance of the user |

#### Return Values:

| Type      | Description                                                             |
| --------- | ----------------------------------------------------------------------- |
| `uint256` | The discount rate, as a percentage - the maximum can be 10000 = 100.00% |

--END--