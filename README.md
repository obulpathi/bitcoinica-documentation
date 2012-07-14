# Bitcoinica reverse-engineering documentation

This document aims at describing the Bitcoinica reverse-engineering findings and describing how the site works and operates.

## License
This work is placed under a WTFPL v2 license.

## General overview
Bitcoinica is a trading platform that works by executing orders against other platforms, mainly MtGox.

## Models

### AdminUser
Users that are allowed to access the administration interface. They are distinct from the actual Bitcoinica users.

### BitcoinAddress
Bitcoin address linked to a user account.

### BitcoinTransaction
Bitcoin transaction as received by the locally running Bitcoin client.

### BitcoinicaCode
Redeemable instrument allowing users to transfer currencies from an account to another.

### Candlestick
### Credential
Not an actual model. Serves as container for class methods used to authenticate against MtGox. **Credentials are hardcoded.**

### Deposit
### InterestRate
### LedgerEntry
### Order
### Position
### Post
### Setting
### Stat
### Ticker
### Trade
### User

## Jobs
### BitcoinDeposit
### BitcoinTransactions
### Candlesticks
### Hedging
### InterestRate
### Liquidating
### Matching
### Redflag
### RestrictingLeverage
### RetryWithdrawal
### Stat
### Swap
### Ticking
### Withdraw

## External dependencies
### Redis
### Resque
Resque is used to manage all the background jobs required to perform various asynchronous tasks.

