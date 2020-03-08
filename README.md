# EOSIO System Contracts

## Dependencies
Please make sure you have installed the below dependencies:
* [EOSIO]()
* [EOSIO.cdt]() (optional, only needed if you need to run the unit test script).

To build the contracts, there are 2 methods:
* [Build contracts using the build script](#build-contracts-using-the-build-script)
* [Build contracts from source code](#build-contracts-from-source-code)

## Build contracts
Clone the repository
```sh
git clone https://github.com/tuan-tl/eosio.contracts.git
cd eosio.contracts
```
### Build contracts using the build script
```sh
cd eosio.contracts
./build.sh
```
### Build contracts from source code
```sh
cd eosio.contracts
rm -fr build
mkdir build
cd build
cmake ..
make -j$NUMBER_OF_PROCESSOR
```
After the above steps, your contracts have been built and stored in `eosio.contracts/build` directory. Each contract has a folder that includes a `wasm` and `abi` file; which will be used for contract deployment on the blockchain.
## References
* _How to build the eosio.contracts_, EOS Developers, viewed 20 Feb 2020, <<https://developers.eos.io/manuals/eosio.contracts/latest/build-and-deploy>>.