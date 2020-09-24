Frequently Asked Questions
==========================
 
What is CHIPS?
--------------

CHIPS is a project started to be implemented in Komodo platform. It is currently one of the few coins that has SegWit and Lightning Network enabled. The objective is for this coin to be used in the Pangea Poker dAPP that is 
currently being developed on Komodo Platform as well as allowing this project to be integrated into any other gaming or gambling system that may want to employ it as it actively supports micro-transactions and has exceptionally 
low fees. Any service that needs to utilize micro-payments can also use CHIPS. 

How will CHIPS be used in the Komodo Platform? 
----------------------------------------------

CHIPS will be the pioneer currency for the decentralized flagship gaming application “Pangea Poker”. Pangea Poker is a truly decentralized Texas hold 'em game application. Komodo coins will be 
exchangeable into CHIPS to be used in the poker game. This will facilitate truly fair decentralized and secured betting and gaming. CHIPS’s use cases don’t stop here though! Any other dAPP or online gaming project that would 
like to utilize the platform is free to do so! CHIPS is a fair launch coin with no premine, allowing for lightning network to be implemented in a fully functional currency, easily adaptable to any online gaming or gambling 
environment. 

What does CHIPS have to do with Pangea Poker?
---------------------------------------------

Although the coin itself doesn’t have a connection with Pangea from a technological point of view, the poker application will be the first focus of the coin’s usage. CHIPS will be the only currency that will be accepted in Pangea Poker – so initially it is going to be exclusive to that 
decentralized application (dAPP).  Pangea poker will be run on the BET platform, which is the technology that will drive Komodo Platform’s gaming module. 

What are some of the features of CHIPS?
---------------------------------------

- Lightning Network enabled
- Microtransactions – used for betting or any other micro-transaction application
- Will be used widely in betting platforms within the Komodo Ecosystem 
- Will be the only currency supported in Komodo Platform’s Pangea Poker 
- Can be integrated into any other gaming system such as online casinos, betting, or incentivized gaming of any type
- Proof of Work phase 
- 10 second block time 

What algorithm is CHIPS based on?
---------------------------------
 
SHA-256 is used for the Proof-of-Work phase as CHIPS is almost a pure BTC fork with lightning network implemented. The block time is 10 seconds. At some point, the coin will switch from PoW to dPoW to ensure that there will never 
be a lack of hashing power for facilitating poker games and to combat a lack of mining as a result from decreasing mining rewards. 

What is the maximum amount of coins for CHIPS?
----------------------------------------------

As this is almost a pure BTC fork, the maximum supply is 21,000,000 coins. Just as BTC, this fork applies halvings starting from 50 Chips per block. 

Is there a block explorer for CHIPS?
------------------------------------

- http://explorer.chips.cash 

Are there any mining pools for CHIPS?
-------------------------------------

There are only about 10,000 CHIPS left for mining. Mining is almost not worth it anymore, a block reward is 0.09765625 at this time of writing and is declining fast.

Which exchanges is CHIPS traded on?
-----------------------------------

- The Komodo Platform’s BarterDEX via atomic swaps 
- https://www.coinexchange.io/market/CHIPS/BTC 

Is there a wallet for CHIPS?
----------------------------

CHIPS is supported in Agama and as Command Line Interface. CHIPS uses the same wallet addresses and private keys as Komodo addresses – so you can create a KMD paper wallet to also store your CHIPS until the integration is 
finished. 

How do I set up the wallet/node on Ubuntu 16.0.4?
-------------------------------------------------

A Quick guide is found in the BTC talk forum written by jl777: 

.. code-block:: shell
   
   sudo apt-get install software-properties-common autoconf git build-essential libtool libprotobuf-c-dev libgmp-dev libsqlite3-dev python python3 zip jq libevent-dev pkg-config libssl-dev libcurl4-gnutls-dev cmake add-apt-repository ppa:bitcoin/bitcoin sudo apt-get update sudo apt-get install -y libdb4.8-dev libdb4.8++-dev
	
   cd
   wget https://dl.bintray.com/boostorg/release/1.64.0/source/boost_1_64_0.zip
   unzip boost_1_64_0.zip
   cd boost_1_64_0
   ./bootstrap.sh
   ./b2
   ./b2 install

   cd
   git clone https://github.com/jl777/chips3
   cd ~/chips3
   ./autogen.sh
   ./configure --with-boost=/usr/local/ 
   cd src
   make -j8 chipsd
   make chips-cli
   cp chips-cli /usr/bin # just need to get chips-cli to work from command line
   # make -> will build everything, including QT wallet
   sudo ldconfig /usr/local/lib # (--- thanks smaragda!)
   ./chipsd -addnode=5.9.253.195 &

   cd
   git clone https://github.com/jl777/lightning
   cd lightning
   make
   daemon/lightning-cli stop; lightningd/lightningd --log-level=debug &
   cd privatebet
   ./m_bet
   ./client or ./host

For further instructions check out the BTC talk thread https://bitcointalk.org/index.php?topic=2078449.0

Are there currently any bounties available for this project?
------------------------------------------------------------

Yes!
The KMD and CHIPS team have open bounties for GUI (-----??????--------) devs.

What will CHIPS be able to do?
------------------------------

One of the major functions of CHIPS is facilitating online gaming and betting through Komodo’s BET platform. 
This will enable decentralized card shuffling by poker dealers for example. Or to avoid overbetting, electronic signatures will allow for locking funds in betting games. More information will be made available as the project develops.

Why wasn’t there more publicity for the launch?
-----------------------------------------------
Initially this project was just a first step towards developing Pangea Poker. Now that it is coming to fruition, the coin needs to be spread and circulating to enable actual game playing and test the system. 
Although Pangea Poker is still far from finished, it’s important to have CHIPS circulating to ensure fair distribution and wide dissemination. At the same time, we want to provide the possibility to integrate the technology into other gaming and betting platforms.

Why wasn’t there an Airdrop or ICO?
-----------------------------------

CHIPS was initially set up as a side project by the lead developer of Komodo Platform. As it has been in development for some time now, it was largely a question of when rather than if this coin would be created. Once the decision was made to actually move forward with CHIPS – jl777 wrote the code and deployed it, posting it on bitcointalk.org. The thread didn’t really get much attention until CHIPS was listed on Coinexchange.io in September of 2017.
jl777 felt that the appropriate way to allow for decentralized distribution of CHIPS would be a 100% no-premine coin that had an open and fair launch from the beginning, allowing miners to mine the coin as was done in the pre-ICO 
crypto era. The idea is that if a pure mining launch coin was good enough for Bitcoin, it was good enough for this project.

Where is the roadmap? Or white paper?
-------------------------------------

At this point there’s no roadmap nor white paper as not deemed necessary as long CHIPS is still in the active development phase without any marketing focus.
The closest thing to a whitepaper can be found here: https://supernet.org/en/resources/updates/chip-and-a-chair-let-s-use-bitcoin-s-lightning-network-to-create-a-poker-game

And there is the `PANGEA whitepaper`_.

Were there any announcements?
-----------------------------

There is the Bitcointalk thread as well as a post on SuperNET about the launch:
https://supernet.org/en/resources/updates/chip-and-a-chair-let-s-use-bitcoin-s-lightning-network-to-create-a-poker-game
https://bitcointalk.org/index.php?topic=2078449.msg20793493#msg20793493

How can I get some CHIPS?
-------------------------

Currently you can either mine CHIPS using some of the pools listed (only about 10,000 CHIPS left for mining) or buy them from exchanges such as coinexchange.io and BarterDEX, Komodo Platform’s exchange technology enabling atomic 
swaps.
Coinexchange.io currently only offers BTC/CHIPS, but BarterDEX provides you with dozens of cryptocurrencies to exchange for CHIPS.

Why implement Lightning Network right now?
------------------------------------------

Because no other coins have truly utilized the full potential of Lightning Network. We believe that implementing LN technology will not only increase efficiency and allow for very low fees, but also enable randomization to provide truly decentralized and fair gaming – such as for the flagship project, Pangea Poker.

What’s the current status of CHIPS, with no GUI wallet and no poker dAPP?
-------------------------------------------------------------------------

It holds and hopefully appreciates in value!
Furthermore, it has the ability to be used by anyone for any technology that requires micro-transactions. As it is nearly a pure hard fork of bitcoin, implementation is easy for those who are familiar with development.

Will the CHIPS use Jumblr?
--------------------------
As it is part of Komodo Platform, Jumblr will be able to be used by trading CHIPS for KMD and then back into CHIPS, in- and outside of BarterDEX. This will increase anonymity as Jumblr employs Komodo as a closed system to prevent any leakage of private information.
BarterDEX will allow for any cryptocurrency, and eventually also fiat currencies, to be exchanged for CHIPS through atomic swaps.

When will Pangea Poker be ready?
--------------------------------
At this point there is no estimated time frame. Currently the focus is on Agama Wallet and BarterDEX, allowing true private, secure, and safe dICOs. Once these technologies are up and running smoothly, development on the poker dAPP will begin with full force. After that, the community will be updated accordingly.

Where can I find more marketing materials?
------------------------------------------
Stay tuned for further announcements on the SuperNET bulletin board and SuperNET Slack channel. Currently there isn’t anything planned except for posting more technical details and neither is troubleshooting a priority for the team at this point. For the moment the team is focusing on completing Agama Wallet and BarterDEX and creating a fully functional ecosystem for other dAPPs.


This FAQ has been written by @Teamcrypton. Addresses for Bounties or Tips:
KMD: RYE7PmuhdggprJFiMBB24sJfVCkXWoSJnd
Chips: RBPxBwTBUrGF2pWkyj9ETY1Bjhhvtrkb6s 

.. _Pangea whitepaper: https://cdn.discordapp.com/attachments/455737840668770315/456036359870611457/Unsolicited_PANGEA_WP.pdf
