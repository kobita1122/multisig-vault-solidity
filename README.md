# Minimal Multi-Sig Vault

A professional-grade Multi-Signature (Multi-Sig) wallet implemented in Solidity. This contract ensures that no single individual has total control over funds, requiring a predefined threshold of owners to confirm a transaction before it can be executed.

## Core Logic
- **Propose**: Any owner can propose a transaction.
- **Confirm**: Other owners can review and sign the transaction.
- **Execute**: Once the threshold is met, the transaction can be triggered.
- **Revoke**: Owners can withdraw their confirmation before execution.



## Security Features
- **Access Control**: Only registered owners can interact with the vault.
- **Threshold Integrity**: The number of required signatures cannot exceed the total number of owners.
- **Reentrancy Protection**: Safe execution patterns used throughout.

## Usage
1. Deploy with a list of owner addresses and the required threshold (e.g., 2-of-3).
2. Deposit ETH or ERC-20 tokens into the contract address.
3. Call `submitTransaction` to propose a spend.
4. Other owners call `confirmTransaction`.
5. Call `executeTransaction` to finalize.
