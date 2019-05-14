Mandatory Update
====================

v1.1.0.0 is a MANDATORY UPDATE for all wallets and masternodes, and all nodes are required to be upgraded by January 31st for them to continue functioning on the latest blockchain.

This release includes a fix for a potential block spam vulnerability (credits to <a href="https://github.com/phoreproject">Phore project</a>), some other bugfixes and upstream merges from PIVX codebase.


How to Upgrade Wallets
--------------
(!) Always backup your wallet.dat before attempting a wallet update (File -> Backup Wallet if you are using the GUI wallet, or copy wallet.dat from the BETTY working directory to the external storage).

If you are running an older version, shut it down. Wait until it has completely
shut down (which might take a few minutes), then run the
installer (on Windows) or just copy over /Applications/BETTY-Qt (on Mac) or
bettyd/betty-cli (on Linux).


How to Upgrade Masternodes
--------------
When upgrading masternodes, upgrade your hot wallet (the one which stores the collateral and receives the rewards) first. Then use the provided script as follows:

 - TODO / J3ll3


1.1.0.0 Changelog
----------------

- [Bug] Segfault with -enableswifttx=0 / -enableswifttx=false
- [Depends] Update Qt download url
- [Qt] More items on the overview page
- [RPC] Segfault pivx-cli getinfo while loading block index
- [Wallet] Block spam vulnerability fix
- [Wallet] Remove potential memory leak, update multisend code


Special thanks
--------

- Giacomo 'giaki3003' Milligan https://github.com/giaki3003/
- Carl 'Cryptosi' Anthony https://github.com/mrcarlanthony

as well as the entire Bitcoin, Dash, PIVX and Phore teams!
