# Smart Wallet Contract

A secure and flexible Ethereum smart wallet contract that implements multi-signature guardian control, allowance management, and secure fund transfer capabilities.

## Features

### 1. Ownership Management
- Single owner control for basic operations
- Guardian-based ownership transfer system
- Requires multiple guardian confirmations (3) to change ownership

### 2. Guardian System
- Guardians can be added or removed by the owner
- Multiple guardians can propose and vote for a new owner
- Guardian consensus is required for ownership transfer

### 3. Allowance System
- Owner can set spending allowances for other addresses
- Allowance tracking per address
- Automatic allowance reduction upon transfers

### 4. Transfer Capabilities
- Direct transfers from owner without restrictions
- Allowance-based transfers for approved addresses
- Support for both simple transfers and contract interactions
- Payload support for complex contract interactions

## Key Functions

### Owner Functions
- `setGuardian`: Add or remove guardians
- `setAllowance`: Set spending limits for other addresses

### Guardian Functions
- `proposeNewOwner`: Propose and vote for a new owner
- Requires 3 guardian confirmations to execute ownership change

### General Functions
- `transfer`: Execute transfers with optional payload data
- `receive`: Accept direct ETH transfers

## Security Features
- Guardian-based recovery mechanism
- Allowance-based spending limits
- Required confirmations for ownership changes
- Protected function access

## Usage

The contract can be used as a secure wallet with the following capabilities:
1. Store and manage ETH
2. Set up trusted guardians for recovery
3. Delegate controlled spending to other addresses
4. Execute both simple transfers and complex contract interactions

## Security Considerations
- Guardian addresses should be carefully selected and verified
- Allowances should be set with appropriate limits
- Owner should regularly verify guardian and allowance settings