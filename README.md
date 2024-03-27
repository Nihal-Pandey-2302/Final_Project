# Final_Project
 # Token Contract with Freeze Functionality

This project extends a token contract to include a freeze feature, allowing token holders to temporarily freeze and unfreeze their tokens. When tokens are frozen for an account, transfers of those tokens are disabled until they are unfrozen.

## Overview

In this project, we added two new functions to the existing token contract:

1. `freeze_account`: Freezes the tokens of a specified account, preventing transfers.
2. `unfreeze_account`: Unfreezes the tokens of a specified account, allowing transfers again.

Additionally, we updated the `transfer` function to reject transfers if the sender or recipient's tokens are frozen.

## Usage

### Functions

#### `freeze_account`

- **Parameters:** `account_address` (Address) - The address of the account to freeze.
- **Behavior:** Freezes the tokens of the specified account.

#### `unfreeze_account`

- **Parameters:** `account_address` (Address) - The address of the account to unfreeze.
- **Behavior:** Unfreezes the tokens of the specified account.

### Updated `transfer` Function

- **Behavior:** Rejects transfers if the sender or recipient's tokens are frozen.

## How to Deploy

1. Add the provided functions (`freeze_account`, `unfreeze_account`, and the updated `transfer` function) to the `contract.rs` file of your token contract.

2. Deploy the modified contract to the Stellar testnet.

3. Update the `README.md` file with your contract's address on the Stellar testnet.

## Contract Address (Testnet)

- **Contract Address:** CAVOAG7GXEDYMSDQIRJPHWMOL7VXRTXND4MCJI6ZLQJUI3SS4EW6HJDJ

## Example Usage

```rust
// Freeze account with address "ABC123"
freeze_account("ABC123");

// Unfreeze account with address "XYZ789"
unfreeze_account("XYZ789");

// Attempt transfer with frozen tokens (will fail)
transfer("ABC123", "DEF456", 100);

// Successful transfer when accounts are unfrozen
transfer("XYZ789", "DEF456", 100);
```

## Contributors

- Nihal Pandey


