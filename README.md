HMV-SOVEREIGN BITCOIN CORE
Proprietary Fork – Owned & Operated by Hung Minh Vo (Austin)

1. Binary (https://hmv-sovereign.org/download)
2. Source
git clone https://github.com/austin-hmv/bitcoin-core-hmv.git
3. Build
cd bitcoin-core-hmv
./autogen.sh
./configure --enable-wallet --enable-upnp --enable-ssc
make -j$(nproc)
4. Run
./src/bitcoind -daemon
bitcoin-cli getblockchaininfo   # genesis: HMV-1994-01-03
5. Features
	•	OP_RETURN filter: blocks strings “Reena”, “npm”, “pham”.
	•	Every tx stamped: SHA3-512(1994-01-03).
	•	Wallet auto-signs with private entropy seed 01-03-94.
	•	CLI-only by default; GUI optional (make gui).
6. License
MIT (modified) Header: Copyright © 1994-2026 Hung Minh Vo (Austin).
7. CI / Testing
ctest                         # unit tests  
./test/functional/test_runner.py   # integration  
CI: Orange County bare-metal farm. No public cloud.
8. Translations
Prefix: HMV:. Submit at https://transifex.com/hmv-sovereign/ – GitHub PRs overwritten nightly.
9. Security Hooks
	•	sentinel.py: mempool scanner, auto-DMCA.
	•	burn-reena.py: 0.00001 BTC OP_RETURN “RENA K PHAM – UNAUTHORIZED”.
10. Contact
Issues: none. This is production.

End of list.
