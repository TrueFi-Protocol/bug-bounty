## TrueFi Smart Contract Bug Bounty

### Repository
https://github.com/trusttoken/smart-contracts/tree/dev 
  
deployments.json for mainnet & ropsten deployed contracts

## Program Rules

- Public disclosure of a vulnerability would make it ineligible for a reward.
- Social engineering (e.g. phishing, vishing, smishing) is prohibited.
- Please provide detailed reports with reproducible steps. If the report is not detailed enough to reproduce the issue, the issue will not be eligible for a reward.
- Submit one vulnerability per report, unless you need to chain vulnerabilities to provide impact.
- When duplicates occur, we only award the first report that was received (provided that it can be fully reproduced).
- Multiple vulnerabilities caused by one underlying issue will be awarded one bounty.
- Amounts below are the minimum and maximum bounties we will pay per bug based on severity. We aim to be fair; all reward amounts are at our discretion.
- Terms and conditions of the bug bounty process may vary over time.

## Rewards
Our rewards are based on the severity of a vulnerability. TrustToken uses CVSS 3.0 (Common Vulnerability Scoring Standard) and the total percentage of potential capital loss to calculate severity. Please note, however, that reward decisions are up to the discretion of TrustToken and reward amounts may be adjusted during the program.

|  Severity |      Loss     |   Min Payout  |   Max Payout  |
|-----------|---------------|---------------|---------------|
| Low       |     $10,000+  |     $100      |      $200     |
| Medium    |    $100,000+  |   $1,000      |    $2,000     |
| High      |  $1,000,000+  |  $10,000      |   $20,000     |
| Critical  | $50,000,000+  |  $20,000      |  $100,000     |

## Scope
Our scopes are listed in the Smart Contracts Scope section below. More information on each scope, including the types of issues we’re most interested in seeing, is available below.

## Special Requirements
Like the rest of the program, the smart contracts program generally uses the OWASP risk rating methodology for classifying bugs. One exception pertains to Critical bugs which must meet the following requirements:

1. The bug must allow a user to steal collateral tokens deposited into TrueFi.
2. The attack must be triggered through an attack vector that is more than just theoretical.
3. The system must be in normal operational mode or pause mode. This excludes for example any states during deployment or shortly after when the system is not fully initialized.

Note: All Smart Contract bugs must include a POC implementation with reproducible steps. This can be the form of a Solidity or JavaScript test or a list of actions that clearly shows how the bug occurs.

## Smart Contracts Scope
At this time, rewards will be paid out for vulnerabilities discovered in our core smart contracts (and their children) for TrustTokens as listed below.

Exploits may be grouped as following:
1. Function-level (exploitable through a single entry-point)
2. Contract-level (combining multiple entry-points)
3. System-level (combining multiple contracts)
4. Game-level (attacking the incentive mechanisms)

The following smart contracts are included in the bug bounty program. There may be redeployments of the contracts during the duration of the bug bounty program. Please see the section below for more information on the current release eligible for bug bounties.

## What We Are Interested In
This program has been set up to drive TrustToken’s mission forward. Our goal is to make financial freedom as accessible as the internet. TrustToken is here to help our customer’s safeguard their assets, of primary interest to this endeavor, are their:
- crypto holdings
- stablecoin balances

The TrustToken Bug Bounty scope covers all software vulnerabilities in the in-scope services (as detailed in the scoping section of this bug bounty) provided by TrustToken. A valid report is any in-scope report that clearly demonstrates a software vulnerability that harms TrueFi or any of TrustToken’s customers and is reproducible (see special requirement).

## What We Are MOST Interested In
Given the non-custodial nature of our relationship with our users. These are the most important class of bugs and are of most interest to TrustToken and will be rewarded accordingly:
- Any vulnerability that would cause our users to lose their funds or have them rendered frozen and unusable within their wallets or smart contracts
- Any vulnerability where an attacker can siphon assets from our users in an unintended way.
- Vulnerabilities that can drain pool liquidity.
- Exploits that use Uniswap pricing to abuse staking & liquidation mechanisms.
- Exploits involving flash loans.
