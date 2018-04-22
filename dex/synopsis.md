Synopsis
========

Code name: Orion Dex

Orion Dex is a decentralized token and contract exchange.  Orion Dex has no custodial or counterparty risk.  The user controls their own fund.  Orion Dex never controls the user's fund.  By using decentralized smart contract, Orion Dex cannot maliciously inappropriate user's fund.

## Uniqueness

Orion Dex is an exchange based on "discrete unit contract" (DUC), a concept that is created here.  In "discrete unit contract" exchange, a user who creates a maker order creates a new contract.  The contract is deployed to the network.  Each make order exists as its own contract.  Another users who wishes to take the contract can simply sends money to this contract address to receive the other side of token.  

## Advantages

One of the biggest issue with smart contract is hacking and unintended use.  A DUC contract will be very compact.  The less code on smart contract, the better.  In addition to reduce the attack surface, DUC contract will be easier to maintain and upgrade.  DUC also provide 1005 transparency to order book.

## Prose Description

The market maker (seller) creates the contract.  The contract will lock the selling token.  When buyer sends the required buying amount to the contract, the swap will take place.

## Structure

Pseuocode of an DUC contract

var tokenSell = {
  amount:
  type:
}

var tokenBuy = {
  amount:
  type:
}

function constructor() {
  lock the tokenSell
}


function exchange() {
  check if coin to buy are received
  send the tokenSell to buyer
  send tokenBuy to seller
}

function cancel() {
  return tokenSell to seller
  delete contract
}
