# EOSIO System Contracts
This is a step-by-step guideline to build EOSIO system contracts.
## Dependencies
Please make sure you have installed the below dependencies:
* [EOSIO v1.8]()
* [EOSIO.cdt v1.6]() (optional, only needed if you need to run the unit test script).

To build the contracts, there are 2 methods:
* [Build contracts using the build script](#build-contracts-using-the-build-script)
* [Build contracts from source code](#build-contracts-from-source-code)

## Build contracts
Clone the repository
```sh
git clone https://github.com/tuan-tl/eosio.contracts.git eosio.contracts-1.8-latest
cd eosio.contracts-1.8-latest
git checkout 1.8-latest
```
### Build contracts using the build script
```sh
cd eosio.contracts-1.8-latest
./build.sh
```
### Build contracts from source code
```sh
cd eosio.contracts-1.8-latest
rm -fr build
mkdir build
cd build
cmake ..
make -j$NUMBER_OF_PROCESSOR
```
After the above steps, your contracts have been built and stored in `eosio.contracts-1.8-latest/build` directory. Each contract has a folder that includes a `wasm` and `abi` file; which will be used for contract deployment on the blockchain.
## References
* _How to build the eosio.contracts_, EOS Developers, viewed 20 Feb 2020, <<https://developers.eos.io/manuals/eosio.contracts/v1.8/index>>.