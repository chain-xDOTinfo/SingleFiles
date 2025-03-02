





EXPLORER
--------

An explorer that already works with this chain is https://bitcoin-explorer.org/.
You can conveniently check the current block height and chain details.






POOL
----

Just point your miner to:

solopool.btcgate.net:3333

Set your username to your Bitcoin address with any or even no worker extension, and any password.


Example:

cgminer -o stratum+tcp://solopool.btcgate.net:3333 -u 1D838JH2NgjF3esHjzUtf9p7cTQRF9H6Mb.0 -p x


Or in your ASIC miner's configuration boxes:

Pool: solopool.btcgate.net

Port: 3333

Username: 1D838JH2NgjF3esHjzUtf9p7cTQRF9H6Mb.0

Password (ignored): x


If you enter an invalid address, you will be rejected.






BITCOIN CORE
------------

Only use the Bitcoin Core source code from the official Bitcoin source (https://bitcoincore.org/bin/bitcoin-core-27.1/bitcoin-27.1.tar.gz).
These customizations are specific to Bitcoin Core version v27.1.0 and have only been tested with this version.
Warning! It is strongly discouraged to use these customizations with any other Bitcoin Core version without further verification and steps.

Replace the downloaded files with the enclosed files or apply the adjustments manually.
Manual customization allows you to follow all the steps and understand them better.

Now compile the source code for your system and according to your requirements.

Warning! Before starting the Bitcoin Core software for the first time, make sure that the default data directory (https://en.bitcoin.it/wiki/Data_directory)
is either empty or specify a different directory.
Otherwise your existing data may be damaged and Bitcoin Core will not work properly.

Start Bitcoin Core, your Bitcoin Core client can now connect to the network.






CHANGELOG
---------

Bitcoin Core Version v27.1.0


Files:

- /doc/man/bitcoin-qt.1
- /doc/man/bitcoind.1
- /src/kernel/chainparams.cpp
- /src/chainparamsseeds.h


Details:


- /doc/man/bitcoin-qt.1

	Line 33 (33)

		-Hash value adjustment (Future adjustment by community)




- /doc/man/bitcoind.1

	Line 31 (31)

		-Hash value adjustment (Future adjustment by community)



- /src/kernel/chainparams.cpp

	Line 78 - 88 (78 - 88)

		-BIP16 exception and Taproot exception commented out
		-BIP height and hash value adjustment


	Line 103 - 108 (103 - 108)

		-BIP9 activation adjustment
		-Hash value adjustment (Future adjustment by community)


	Line 121 - 122 (121 - 122)

		-Estimated storage requirements adjustment (Future adjustment by community)


	Line 134 - 142 (134 - 145)

		-DNS-Seeder adjustment (Some of the currently active DNS-Seeder - future extension/adjustment by community)


	Line 159 - 171 (162 - 165)

		-Checkpoint value adjustment (Future checkpoint extension by community)


	Line 180 - 183 (174 - 177)

		-TX value adjustment (Future adjustment by community)




- /src/chainparamsseeds.h

	Line 10 - 1755 (10 - 62)

		-Mainnet seeds adjustment (Some of the currently active seeds - future extension/adjustment by community)
