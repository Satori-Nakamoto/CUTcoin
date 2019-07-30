1/ What is CUTcoin?
CUTcoin is a new anonymous cryptocurrency with PoS consensus. The CUT coin provides users' transactions in an 
absolutely secure way with all private benefits. Another obvious benefit is a PoS consensus.

2/ What does CUTcoin mean?
CUT coin is an abbreviation means "Concealed Untraceable Transaction" Coin. Simply. 

3/ Is CUT coin PoW or PoS (Proof-of Stake) coin?
Proof - of - Work consensus have been chosen as initial coin distribution supply mining method. Current consensus 
is Proof-of-Stake with stakes earned in wallets. 

4/ Which algorithm (algo) is used?
Byzantine Berserker. We are using totally re-written algo.

5/ How many team members?
CUT coin team is about 4 totally involved persons, that's more than enough. 

6/ Why I can't find information about the country origin and team members? Why It's concealed?
CUT coin is about anonymity. Please respect the choices made by each individual on this matter. 
As a community-based project, with no ICO, the lack of corporatization is key, anyone can contribute 
to this project and is highly encouraged to do so. 

7/ How I will receive stakes at PoS?
You will earn stakes on your wallet. 

8/ When exchange?
We are already listed at some good exchanges ;)

9/ After PoS began where it will be possible to buy CUTcoin? Or to get?
Check exchanges. Also, you can get CUT coins taking part in bounty campaign. 

10/ What about [the fake stake attacks](https://medium.com/@dsl_uiuc/fake-stake-attacks-on-chain-based-proof-of-stake-cryptocurrencies-b8b05723f806) of POS coins?
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

So, resuming all we can sure you, that we made researches for this issues and in our PoS code there would be no such issues. [Our POS can be found here.](https://www.reddit.com/user/CUTcoin/comments/aumb8b/cutcoins_proof_of_stake_implementation/)

11/ Quote from: D1f1c0lt 
Why did you decide to switch to PoS from PoW? Just for the sake of ecology and prevention of 51% attack? 
Anyway, you probably know about the drawback of PoS i.e. richer get richer since they possess the most stakes. 
Don't you think it is something unfair though?
Thanks for reply

Sustainability against 51% attack itself is good enough prize to fight for, isn't it? If somebody (or some group) hols 51%+ of mining power that not only able to perform multiple spending but also can change blockchain history on their behalf. In PoS it is unlikely that a person that holds 51%+ of coins being on stake would try to perform malicious manipulations as it evolves in a dramatic decrease of the coin market price.

In CUTcoin  PoS, the probability to obtain a reword is proportional to the number of coins being on stake, so it's not 'richer get richer' in the long term. In the short term, it's clear that the block forging is subject to change and those who put on a stake not much and still forge a block can easily double their CUTcoins.

12/ Was it you guys that found and responsibly disclosed that vulnerability in Monero?
Why yes, [yes it was.](https://cutcoin.org/newmonero)

