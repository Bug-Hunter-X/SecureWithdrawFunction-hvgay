# Reentrancy Vulnerability in Solidity Withdraw Function

This repository demonstrates a common reentrancy vulnerability in a Solidity smart contract's withdraw function and its solution.  Reentrancy attacks can lead to significant loss of funds.

## Vulnerable Contract (bug.sol)
The `bug.sol` file contains a withdraw function susceptible to reentrancy.  The attacker can exploit this by calling a malicious contract that re-enters the `withdraw` function before the balance is updated.

## Solution (bugSolution.sol)
The `bugSolution.sol` file provides a secure implementation of the withdraw function using the Checks-Effects-Interactions pattern to mitigate the reentrancy vulnerability.