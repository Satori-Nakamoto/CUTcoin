## 1. What is CUTcoin?
CUTcoin means "Concealed Untraceable Transaction" Coin . It's a new anonymous cryptocurrency with PoS consensus. 

## 2. Is CUTcoin PoW or PoS?
CUTcoin started out as a PoW coin that used CUTcoin's own hashing algorithm. On March 7th, 2019 at block 52 000, CUTcoin switched to PoS.

## 3. Was there a premine?
Yes, there was a premine of 2% (4M coins). 9.3% of the coins were minted during the PoW phase (18 506 411 CUT) which leaves 88.7%
for the PoS era, or 179 493 589 CUT. About 300 CUT are minted every 2 minutes, and after total supply of 200M is reached, tail emission of 0.6 CUT per block will begin.

## 4. Was it you guys that found and responsibly disclosed that vulnerability in Monero?
Why yes, [yes it was.](https://cutcoin.org/newmonero)See the [hackerone post here.](https://hackerone.com/reports/501585)

## 5. How does staking work?
Here's [an explanation of it.](https://www.reddit.com/user/CUTcoin/comments/aumb8b/cutcoins_proof_of_stake_implementation/)

## 6. How many team members are there?
Currently there are 4 full time CUTcoin developers, and new community members are joining and contributing all the time! 

## 7. Why can't I find personal information about the team members, or their country of origin?
First of all, CUT coin is about anonymity. Second, since crypto regulations have not been finalized and vary widely from country to country, the devs staying anonymous allows them to focus completely on the underlying technology. This way they can continue pushing the limits of concealed, untraceably transactions without worrying about changing laws or market conditions. And finally, CUTcoin is a community-based project with no ICO. The lack of corporatization is key, anyone can contribute to this project and everyone is highly encouraged to do so. 

## 8. How I will receive stakes with PoS?
You will earn stakes directly to your wallet each time you stake a block when you have staking activated. If you have several accounts in your wallet, keep in mind that you will only be staking *on the selected account* when you activate staking. All other outputs in other accounts will not be eligible for forging new blocks a.k.a. receiving stake rewards.

## 9. When exchange?
We are currently listed on STEX, CREX24, p2pb2b and bitalong. As the project progresses we look forward to growing our community and being listed on more exchanges.

## 10. What about [the fake stake attacks](https://medium.com/@dsl_uiuc/fake-stake-attacks-on-chain-based-proof-of-stake-cryptocurrencies-b8b05723f806) of POS coins?

A group of researchers has identified some vulnerabilities in cryptocurrencies based on the Proof-of-Stake principle, especially these vulnerabilities are typical for coins based on PoSv3 (Proof-of-Stake version 3). The fact is that PoSv3 does not provide complete data validation before using resources (disk and RAM). This leads to the fact that an attacker, even without possessing powerful resources, can provoke a node failure by filling its disk and RAM with fake data.
The researchers concluded that all cryptocurrencies based on the UTXO model are vulnerable to attacks called “Fake Stake”.

Vulnerability 1
It was found that Qtum, Particl, Navcoin, HTMLcoin and Emercoin cryptocurrency demonstrated a fairly simple form of this vulnerability - they don’t check the cryptocurrency transaction at all before fixing the block in RAM or disk.
These five cryptocurrencies apply a function in which there is a distribution of blocks and division into blocks and headers. The node requests the block after the header has received an acknowledgment. And given that the node can not independently verify the title - it stores it in the memory structure.
As a result, any attacker can fill the RAM of the node, even has no stake.
The second type of this attack can be performed on the same basis, but it is aimed at the disk (not RAM). Presumably, an attack directed to the disk will be more harmful to the victim if the RAM is full, then you can simply reload the node. But if the disk is full, more serious intervention will be required.

Vulnerability 2
The working group noticed that the first vulnerability was possible using the “header first” feature and the PoSv3 principle. But the attack does not work on earlier versions (for example, Peercoin), because before checking the blocks on the disk, preliminary checks are carried out: checking the output to the main circuit and checking the compliance of the PoS kernel hash.
But in later versions there may be some problems.
First, the verification guarantees that the coin only exists, but does NOT guarantee that it is not spent.
Secondly, even if you check the block on the divergence of the main chain, the transaction of the recipient of the coin is checked by TxDB for the main chain itself.
To bypass the main circuit output check, you can use a pin that is not yet verified by the node, but has already been spent. To bypass the verification of the PoS kernel hash, you need to extract a valid block that passes the goal of complexity, which in turn would require a large number of stakes. However, as it turns out, incomplete checking can be abused to generate an arbitrary number of visible stakes.

So rest assured, we have researched this issue, tested our code and in our PoS code there is no such issues. [Our POS can be found here.](https://www.reddit.com/user/CUTcoin/comments/aumb8b/cutcoins_proof_of_stake_implementation/)

## 11. "Why did you decide to switch to PoS from PoW?" 
"Just for the sake of ecology and prevention of 51% attack? Anyway, you probably know about the drawback of PoS i.e. richer get richer since they possess the most stakes. Don't you think it is something unfair though?" (Question from D1f1c0lt)

Sustainability against 51% attack itself is good enough prize to fight for, isn't it? If somebody (or some group) hols 51%+ of mining power that not only able to perform multiple spending but also can change blockchain history on their behalf. In PoS it is unlikely that a person that holds 51%+ of coins being on stake would try to perform malicious manipulations as it evolves in a dramatic decrease of the coin market price.

In CUTcoin  PoS, the probability to obtain a reword is proportional to the number of coins being on stake, so it's not 'richer get richer' in the long term. In the short term, it's clear that the block forging is subject to change and those who put on a stake not much and still forge a block can easily double their CUTcoins.
 
## 12. Does reward received from previous stake automatically consider for forging next block?
No, the staking reward **and the output used to forge the block** must wait 800 blocks to mature.

## 13. Must user stop staking in order to send? Will the wallet stop staking after sending funds?
No, the user can send normally without stopping staking. When you send funds you create a transaction which, like all transactions, has inputs and outputs. Once this transaction is added to the blockchain 800 blocks must pass before these specific outputs start participation in forging. To make it more clear, let's look at how the process of staking is implemented in the wallet. Each time a new block appears, the wallet looks for unspent outputs from the opened account that can participate in staking and checks that they meet several conditions: the output amount must be >= 1CUT, the age in the blockchain is >= 800. So all outputs that meet these conditions automatically participate in staking (and it is reflected in the statistics updates), no additional actions required. Transaction change, like any other outputs, must wait for 800 blocks.

## 14. Help! I lost my coins!

Before you start (or continue) to panic, check these common mistakes:
- Is your wallet fully synched?
  - Wallets must be fully synched (100%) to display the latest blockchain transactions.
  - Side note: A wallet can't send unless it's connected to a fully synchronized daemon.
- Does the creation height of your wallet preceed the first transaction of that wallet?
  - If you are importing a wallet, make sure that the "wallet creation height" is less than the blockchain height of your first transaction. For example, if your first transaction is on block 201538 then your wallet creation height should be set to < 201538, for example 201000.
- Check if the transaction shows on the blockchain. If it does, then the coins are in the right place and the problem is with the wallet or exchange. This is how you [use the block explorer.](https://www.reddit.com/r/cutc0in/comments/dmjsm3/cli_guides_using_the_block_explorer/) note: the guide is written for the CLI wallet. With GUI wallet it's more simple. 
- "I sent coins to / from exchange and now they vanished!"
  - This is a problem with the exchange, not with the CUT network or wallet. Some exchanges have a delay before they even show a deposit as "incoming". Sometimes this delay is quite long, like with CREX24 for example. It's the same with withdrawals. Use the block explorer to verify that the coins are where they should be, and have some patience.
- Withdrawal from official staking pool is not going through / taking forever.
  - Firstly, for security reasons, all the coins are not held in the hot wallet. The majority of coins staking are on a secret server that only the pool admins know about. Although it slows down withdrawals, this is a **must** for security. Secondly, due to the pool's algorithm, withdrawals suffer a slight delay. Thirdly, if there are a lot of withdrawals at the same time then it will cause a traffic jam in the pool's wallet, since the change from each output needs to wait 10 blocks to become spendable. Large withdrawals will take a long time, and please keep in mind that the staking pool is primarily meant for stakers with a small amount that want to eliminate low probability risk. It will always be more profitable to stake on your own, as long as you have a stable device with a stable internet connection.
