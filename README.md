AmeToken🍭 is a sample token we use in Ropsten for testing ERC20 token transactions. The contract is almost the same with [the Dai token contract in mainnet](https://etherscan.io/address/0x6b175474e89094c44da98b954eedeac495271d0f#code).
_beware that it is NOT [the Sai token contract in mainnet](https://etherscan.io/address/0x89d24a6b4ccb1b6faa2625fe562bdd9a23260359)_

Here are two changes I made:
- I replaced "Dai" with "Ame".
- I added the `uint256 _initialAmount` argument in the `constructor`. `_initialAmount` is added to `msg.sender`'s balance(see the code below). I deployed from my account, and thus `msg.sender` is my account.
```solidity
constructor(uint256 _initialAmount, uint256 chainId_) public {
    balanceOf[msg.sender] = _initialAmount;    
```

The AmeToken address is `0x0B01c339DFAEad1F70b70A554344993D27Cbc498`.

Here is [a link](https://ropsten.etherscan.io/address/0x0b01c339dfaead1f70b70a554344993d27cbc498) to the AmeToken in Etherscan.

You can read the whole code in ./AmeToken.sol
