# MoeyEx
A Volatility 3 plugin for extracting Monero’s account base instances.

(Monero stores wallet-related key data in the account_base instance)

## Features
MoeyEx extracts key values(Public/Private keys) from memory dump files.

The output data is as:

- Public Spend Key 
- Public View Key 
- Private Spend Key  
- Private View Key 
- Creation Time

## Use instructions



# Decrypt wallet keys file
The wallet keys file encrypts and stores key values and wallet-related setting data.

## Features

## Use instructions
    python decrypt_keys_file.py --file=<file-path> --password=<wallet-password"

# Decrypt wallet cache file
The wallet cache file encrypts and stores transactions data related to imcoming, outgoing.

(The code can be decrypted for wallets that do not have an unconfirmed transaction and do not use subaddress and multisignature)

## Features

## Use instructions
    python decrypt_cache_file.py --file=<file-path> --password=<wallet-password"
