Multi masternode config
=======================

The multi masternode config allows you to control multiple masternodes from a single wallet. The wallet needs to have a valid collateral output of 1000 coins for each masternode. To use this, place a file named masternode.conf in the data directory of your install:
 * Windows: %APPDATA%\BETTY\
 * Mac OS: ~/Library/Application Support/BETTY/
 * Unix/Linux: ~/.betty/

The new masternode.conf format consists of a space seperated text file. Each line consisting of an alias, IP address followed by port, masternode private key, collateral output transaction id, collateral output index, donation address and donation percentage (the latter two are optional and should be in format "address:percentage").

Example:
```
mn1 127.0.0.2:34120 7i5S8We5d7E2WRVTyizNX1ytjEf5iR5ChbyT4dp6399G2ZW6zjF f96bb531c80617c1214c248aad6d0ac1ad6b1e6081627864b164be7048dc5dc3 0
mn2 127.0.0.3:34120 7iVhkVB2UZbrTXtyPnQgPCU6carsyuKGaFy2WczwmxoLCuJZnmP 288dc8426ed92a9446ee4d6cc95edfa0e9ffa1ac7661f1fb1089f75b3c01a38c 0 PKFhiRbVYkhPgTNYJQKE9KuwTDbSGaXXWA:33
mn3 127.0.0.4:34120 7ivG5EsKgqvQrKEQWHvnzE9GFrKcb5WT8HiVQWbvuF4XUmYY6YT 9cd14c950be9757f2d9c27fdced08b67c2bfa910c79dd6ee1dcc2110951454c7 1 PRkzWQdhUWgAmaDnHeRaEiPGpbeuDWHSUy
```

In the example above:
* the collateral for mn1 consists of transaction f96bb531c80617c1214c248aad6d0ac1ad6b1e6081627864b164be7048dc5dc3, output index 0 has amount 1000
* masternode 2 will donate 33% of its income
* masternode 3 will donate 100% of its income


The following new RPC commands are supported:
* list-conf: shows the parsed masternode.conf
* start-alias \<alias\>
* stop-alias \<alias\>
* start-many
* stop-many
* outputs: list available collateral output transaction ids and corresponding collateral output indexes

When using the multi masternode setup, it is advised to run the wallet with 'masternode=0' as it is not needed anymore.
