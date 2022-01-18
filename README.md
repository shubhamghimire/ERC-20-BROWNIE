# 100-Days-of-Blockchain-Development

## Day-1 2021/11/28
 - Started the "Solidity, Blockchain and Smart Contracts" course on freecodecamp channel in youtube (https://www.youtube.com/watch?v=M576WGiDBdQ&t=219s)
 - Smart Contracts are self executing sets of instructions, without 3rd parties.
 - NFT (Non-fungible tokens) ---> Smart contracts that live on a blockchain.
 - Crypto coin vs Tokens. (Coin --> Etherium, Token --> ERC20)
 - 'The Oracle' problem in smart contracts.
 - Hybrid smart contracts ---> 'Chainlink' protocol. ---> Oracle network.
 - Blockchain Features:
    - Decentralized
    - Transparency and Flexibility
    - Speed and Efficiency
    - Security and Immutability
    - Removal of counterparty risk.
    - Trust Minimized Agreements.
    - Hybrid smart contracts combine on and off chain.
- Donwloaded and setup metamask.io wallet.
- Use of testnets like rinkeby and kovan on metamask.
- Faucet application which gives us free test tokens. For example, free test Rinkeby Etherium.
- Etherscan.io (Block Explorer) - An application that allows us to view transactions that happen on a blockchain.
- Gas --> Measure of computation fee.
    - Gas Price --> How much it costs per unit of Gas?
    - Gas Limit --> Max amount of Gas in a transaction.
    - Transaction fee --> Gas Used X Gas Price (i.e. 21000 Gas @ 1 GWEI per gas = 21000 GWEI)
- Gas price is based off the "demand" of the blockchain.
- The more people want to make the transaction, the higher the Gas price, and therefore the higher the transaction fees.
- Etherium Hashing Algorithm --> keccak256
- The first block of the blockchain is called the "Genesis Block".

#### Mining
- The process of finding the "solution" to the blockchain problem.
- Nodes get paid for mining blocks.
- Etherium uses "Elliptic Curve Digital Signature Algorithm" for private and public keys.
- Public Key is derived from your private key. Anyone can see it, and use it to verify that a transaction came from you.
- "Signing a transaction" ---> A one way process. someone with a private key signs a transaction by their private key being hashed with their transaction date. Anyone can then verify this new transaction hash with your public key.
- Node is a single instance in a decentralized network. 
- Proof of work and proof of stake.
- Consensus is a mechanism used to agree on the state of a blockchain.
- Sybil Resistance mechanism.
- Transaction fee --> Paying blockchain nodes for including transaction.
- Block reward is given to the block by blockchain itself.
- Longest chain rule.
- 51 % attack.


## Day-2 2021/11/29
- Solidity programming for creating smart contracts.
- Remix IDE for solidity programming.
- Data types in solidity programming language.
 - uint256, int256, bool, string, address, bytes32
- Default initializations of variables.
- Comments in solidity using '//' sign.

## Day-3 2021/11/30
- Creating functions in solidity.
- Visibility --> external, public, internal, private
- NFT (Non-fungible tokens) and DeFi (decentralized finance)

## Day-4 2021/12/01
- Function calls are transactions.
- View and pure functions. Public variables are always view functions. 
- Pure functions are functions that do some type of pure math.
- View function declares that no state will be changed.
- Pure function declares that no state variable will be changed or read.

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.3;

contract ViewAndPure {
    uint public x = 1;

    // Promise not to modify the state.
    function addToX(uint y) public view returns (uint) {
        return x + y;
    }

    // Promise not to modify or read from the state.
    function add(uint i, uint j) public pure returns (uint) {
        return i + j;
    }
}
``` 

- Structs are useful for grouping together related data. Structs can be declared outside of a contract and imported in another contract.

```
pragma solidity ^0.5.0;

contract test {
   struct Book { 
      string title;
      string author;
      uint book_id;
   }
   Book book;

   function setBook() public {
      book = Book('Learn Java', 'TP', 1);
   }
   function getBookId() public view returns (uint) {
      return book.book_id;
   }
}
```

- Storage and Memory keywords in Solidity are analogous to Computer’s hard drive and Computer’s RAM. Much like RAM, Memory in Solidity is a temporary place to store data whereas Storage holds data between function calls. The Solidity Smart Contract can use any amount of memory during the execution but once the execution stops, the Memory is completely wiped off for the next execution. Whereas Storage on the other hand is persistent, each execution of the Smart contract has access to the data previously stored on the storage area. 

## Day-5 2021/12/02
 - Mapping is a reference type as arrays and structs. Following is the syntax to declare a mapping type.
    ```
    mapping(_KeyType => _ValueType)
    ```

    Where,

        -_KeyType − can be any built-in types plus bytes and string. No reference type or complex objects are allowed.

        -_ValueType − can be any type.
- SPDX License identifier at the top of the solidity code.
- Deploying my first contract on rinkeby network (SimpleStorage.sol) and interacting with the deployed contract.
- Successfully deployed a contract from another contract in a blockchain. 

## Day 6 2021/12/03 and Day 7 2021/12/04
- Interacted with a deployed contract.
- 'StorageFactory.sol' code pushed.
- Binance account open and verification completed.
- Learned about crypto tax in Japan.

## Day 7 2021/12/05
- Investigated about 'Polkadot' and its technology.

## Day 8 2021/12/06
- Watch technical analysis on daily prices on 'Polkadot'.
- Decentralized oracle chain network.
- Deterministic and non-deterministic approach. 
- Why blockchains can't use APIs? Because when calling API from every node the result can vary so that each node has different values when validating.
 - Chainlink is a modular decentralized oracle infrastructure and oracle network that allows us to get data and do external computation in a highly civil resistant decentralized manner. 
 - Decentralized data feeds for the hybrid smart contract ecosystem. (data.chain.link)

 ## Day 9 2021/12/07
 - Implemented a function to get the latest price of etherium and USD. (https://docs.chain.link/docs/get-the-latest-price/)
 - Implementing data feed in fundme application.
 - Importing 'chainlink' code on main codes.
 - Interfaces compile down to ABI (Application Binary Interface). The ABI tells solidity and other programming languages how it can interact with another contract.
 - Contract call using interfaces.
 - Modifier is used to change the behavior of a function in a declarative way.
 - Created and pushed a crowdsourcing funding application and pushed it 'FundMe.sol'.
 
 ## Day 10 2021/12/08
 - Limitations of Remix IDE.
 - Starting with web3.py python package.
 - Setup VS Code for python and solidity development.
 - Reading solidity file in python program. 
 - 'py-solc-x' for compiling solidity in python.
 - JSON ABI and formattiang JSON.

## Day 11 2021/12/09
- Deploying in 'Local Gnache' simulated blockchain.
- Connecting to 'Gnache Blockchain' from the user interface.
- 'Proof of History' concept in Solana. 'Time Keeping' phenomenon in blockchain. [https://www.youtube.com/watch?v=_ivdpGSloaY]
- HTTP / RPC Provider for connecting to gnache simulated blockchain.
- Setup environment variables to store private key values.

## Day 12 2021/12/12
- Creating and storing environment variables for private keys for security purpose.
- Using Python-dotenv package to access environment variables in python code.
- Signing a transaction that is deploying a contract to the blockchain.
- Viewing our Transaction / Deployment in Ganache and waiting for Block Confirmations.
- State change of the contract deployed on the local blockchain.
- Using 'Gnache CLI' instead of user interface. Use 'ganache-cli' to start ganache instance.
- 'infura.io' is a platform which gives you a blockchain url for you to connect with and run your blockchain on a testnet. Alternative is 'alchemy.com'. 
- ENS Domains. ENS is just like DNS for web3. We remeber 'google.com' instead of the long ip address of google. Like that we remeber the ENS domains instead of the etherium address of a person. We can send crypto or nft in the 'shubham.eth' instead of sending to the address.
- Installing Brownie (Brownie is a Python-based development and testing framework for smart contracts targeting the Ethereum Virtual Machine.)
    - Install pipx
    - pipx install eth-brownie
    - Testing Successful Install
-Brownie Simple Storage Project
    - A new Brownie project with brownie init
        -Project Basic Explanation
    Adding SimpleStorage.sol to the contracts folder
    - Compiling with brownie compile
    - Brownie deploy script
        -def main is brownie's entry point
    - brownie defaults to a development ganache chain that it creates
    - Placing functions outside of the main function
    - brownie accounts
        - 3 Ways to Add Accounts
            -   accounts[0]: Brownie's "default" ganache accounts
                - Only works for local ganache
            - accounts.load("..."): Brownie's encrypted command line (MOST SECURE)
                - Run brownie accounts new <name> and enter your private key and a password

## Day 13 2021/12/13
- Creating 'brownie-config.yaml' to initialize the private key saved in environment file.
- accounts.add(config["wallets"]["from_key"]): Storing Private Keys as an environment variable, and pulling from our brownie-config.yaml
    - You'll need to add dotenv: .env to your brownie-config.yaml and have a .env file
- Importiang a contract in brownie.
- Deploying a contract from brownie.
- Writing smart contracts tests in Python.
- A test setup is in the following order:
    - Arrange
    - Act
    - Assert
- Testing commands:
    - 'brownie test -k function_name': Only tests the function in the test script.
    - 'brownie test --pdb": If test is failed, python shell will pop up to debug the variables in the test.
    - 'brownie test -s": More robust and detailed information.
    - Use pytest documentation for reference.

## Day 14 2021/12/15

- Deploying brownie to a testnet.
- 'bronie networks list' [Compatible networks with brownie].
- Development vs Ethereum
    - Development is temporary
    - Ethereum networks persist
- RPC URL / HTTP Provider in Brownie

## Day 15 2021/12/16

- Accessing previous deployments in rinkeby network using infura.io
- Interacting with contracts deployed in our brownie project.
- Using brownie console to interact with functions.

## Day 16 2021/12/17

- Setup development environment and dependencies for brownie fund me project.
- Set path for chainlink-brownie-contracts. (https://github.com/smartcontractkit/chainlink-brownie-contracts)
- Creating Deploy Script (V1)
- 'helpful_scripts.py' for pulling accounts for deployments
- Importing functions is easy using __init__.py


## Day 17 2021/12/18
- Deploying the brownie fund me project to Rinkeby test network.
- Contract verification in rinkeby.etherscan.io
    - Manual Verification ("Flattening")
        - Copy paste all the solidity codes into etherscan. Remove any imports and instead of the imports write the actual codes. All coodes should be in a single file.

    - The Programmatic Way
        - Create an account to etherscan.io and get the API key.
        - Deploy the contract and see the codes and interact with the contract in rikeby.etherscan.io
    - Interacting with Etherscan
- Deploying to Local Chains
- Intorduction to Mocking.
- Constructor parameters.
- 'networks' in our 'brownie-config.yaml'.
- Copying mock contracts from chainlink-mix.[https://github.com/smartcontractkit/chainlink-mix/blob/master/contracts/test/MockV3Aggregator.sol]
- Understand little bit about metaverse. Find some technics on how to start on the metaverse.
    - Find initial projects and join their discords and chat with them.
    - Help their community in any way from answering questions in discords to playing their game.
    - Search and play a lot of metaverse games and try to build something if you know the development method.



## Day 18 2021/12/19
- Files were not organized in the brownie_fund_me project folder. Organized the scripts and files according to the tutorial.
- Deploying the mocks on the local development environment.
- Cleaning up the deploy.py script so that it look nicer and easier to read and understand.
- Deploying to a persistent ganache.
- Adding a persistent brownie network.
    - 'brownie networks add Etherium ganache-local host=http://127.0.0.1:7545 chainid=1337'

## Day 19 2021/12/21
- Recommended suggestions by the 'Mepalease Crypto Community'.
    - Blockchain Development Course by University of Nicosia(https://www.unic.ac.cy/blockchain/).
    - Alpha coins: The coins which is open source. The coin run by community which does not have any CEO. The coin has great future. For example, Dogecoin.

- Mocking Solidity contracts for testing(https://ethereum.org/en/developers/tutorials/how-to-mock-solidity-contracts-for-testing/).
- Resetting a network build by deleting mock chain id from build/deployments/map.json and deleting the chain-id folder.
- Fund and withdraw scripts executed and tested. [scripts/fund_and_withdraw.py]
- Test script executed to test the functions of fund and withdraw.

## Day 20 2021/12/22
- Installing pytest for testing.
- Using 'pytest.skip' to execute the test skipping conditions.
- Forking in blockchain. Copying a blockchain and creating a network is called blockchain fork.
- Mainnet fork in brownie.
- Where should I run my tests?
    - Brownie Ganache Chain with Mocks: Always
    - Testnet: Always (but only for integration testing)
    - Brownie mainnet-fork: Optional
    - Custom mainnet-fork: Optional
    - Self/Local Ganache: Not necessary, but good for tinkering

## Day 21 2021/12/23
- Started smart contract lottery project.
    - Created github repo for the project.
    - Created brownie environment for the project.
- Creating Lottery.sol contract and adding lottery functions.
- Added config to the brownie-config.yaml.

## Day 22 2021/12/25
- Chainlink price feed added.
- Getting entrance fee function code added.
- Testing the entrance fee calculation execution code.
- Smart contracy lottery app created in alchemyapi.io for testing the etherium mainnet connection.
    - brownie networks add development mainnet-fork cmd=ganache-cli host=http://127.0.0.1 fork=https://eth-mainnet.alchemyapi.io/v2/rAOJmQC42FUIQryzVR1PfkZuv3-th6VL accounts=10 mnemonic=brownie port=8545
- Enums are the way of creating user-defined data types, it is usually used to provide names for integral constants which makes the contract better for maintenance and reading. Enums restrict the variable with one of few predefined values, these values of the enumerated list are called as enums. Options of are represented with integer values starting from zero, a default value can also be given for the enum. By using enums it is possible to reduce the bugs in the code.

## Day 23 2021/12/26
- Adding openzeppelin access controls for admin authorization purpose.
- Open Zeppelin is the standard for secure blockchain applications. OpenZeppelin provides security products to build, automate, and operate decentralized applications. We also protect leading organizations by performing security audits on their systems and products.

## Day 24 2021/12/30
- Fixing the openzeppelin error.
- Adding codes to end lottery function to choose the lottery winner.
-  Getting truly random number in a deterministic system is impossible.
- Malicious RNG operators are a risk.
- 'msg.value' and 'msg.sender' are global variables which are vulnerable from security perspective.
 
 ## Day 25 2022/01/04
 - Doing Research on a Cryptocurrency Coin or Token.
    - Technical Analysis
        - Study of the past price of an asset.
        - Reading Charts and Finding Patterns
    - Sentimental　Analysis
        - Study of what everyone is feeling about a stock.
        - What are crypto influencers saying about a project.
    - Fundamental Analysis
        - Study of the actual ideas, team, and progress of a specific project.
- Best practices on working with random numbers.
- Chainlink VRF provides verifiable randomness. (https://docs.chain.link/docs/chainlink-vrf/)
- Getting a random number inside a smart contract using Chainlink VRF. (https://docs.chain.link/docs/get-a-random-number/)


 ## Day 26 2022/01/05
- ETH --> Pay some ETH gas, transaction gas
- LINK --> Pay some Link gas, oracle gas
- Running the random number generation code using Link tokens in kovan network. (https://remix.ethereum.org/#url=https://docs.chain.link/samples/VRF/RandomNumberConsumer.sol)
- Basic request and receive cycle of getting data while generating random number. (https://docs.chain.link/docs/architecture-request-model/)
- Two asynchronous transactions while calling random number function. 
- Importing VRF consumer base code into the lottery code file. (https://github.com/smartcontractkit/chainlink/blob/develop/contracts/src/v0.6/VRFConsumerBase.sol)

## Day 27 2022/01/06
- Keyhash is the unique way to identify chainlink VRF node. 
- Picking up random winners out of list of players in smart lottery contract.
- Modulo operation in solidity.
    '''
    contract Mod {
        uint256 public number = 5;

        function doMod(uint256 modvalue) public view returns(uint256){
            return 5 % modvalue;
        }
        // divides by the number, and returns the remainder
    }
    '''
- Completed smart contract lottery.sol code and moving to testing phase.

## Day 28 2022/01/08
- deploy_lottery.py and helpful_scripts.py scripts added.
- get_account() function in helpful_scripts.py refactored.
- get_contract() function in helpful scripts added.
    - This function will grab the contract addressed from the brownie config
    if defined, otherwise it will deploy a mock version of that contract, and 
    return that mock contract. 

## Day 29 2022/01/09
- get_contract() function
   -  contract_to_mock
   -  Contract.from_abi

## Day 30 2022/01/10
- Adding the parameters to deploying to lottery
- vrfCoordinatorMock and adding mocks.
- Added 'Link Token' address for Rinkeby.

## Day 31 2022/01/11
- Successfully deployed MockV3Aggregator, LinkToken, VRFCoordinatorMock and Lottery.
- 'start_lottery' function added.
- 'enter_lottery' function added.
- 'end_lottery' function added.

## Day 32 2022/01/13
- 'LinkTokenInterface' Creation in smartcontract lottery project.
- Finished the smartcontract lottery project.
- Creating unit tests and integration tests of the smart-contract-lottery project.
    - Unit Tests: Development Network
    - Integration Tests: Testnet
- 'test_lottery_unit.py' created.
    - Test Command: 'brownie test -k test_get_entrance_fee'

## Day 33 2022/01/15
- Using pytest.skip to run tests only when working on the local environments.
- Creating unit test to test the lottery starting, entering, ending, choosing winners mechanism.

## Day 34 2022/01/16
- Events and logs in solidity.
- Sucessfully created test function to test the lottery winner picking and paying mechanism.
- Creating intergration tests fot the smartcontract-lottery.
    - Testing on a live rinkeby chain.
    - Integration test completed and passed.
- Deploying smart-contract lottery to an actual testnet.

## Day 35 2022/01/17
- Brownie mixes for project boiler codes. (https://github.com/brownie-mix)
- Creating chainlink-mix project using brownie mix.
    - 'brownie bake chainlink-mix'

## Day 36 2022/01/18
- ERC 20 Tokens
    - ERC (Etherium Request for Comments)
    - https://eips.ethereum.org/EIPS/eip-20
    - https://docs.openzeppelin.com/contracts/4.x/erc20
- Creating your own ERC-20 Token.
    - https://moralis.io/how-to-create-your-own-erc-20-token-in-10-minutes/
    


















  