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
1. py-cryptonight install
   - Run cmd in the py-cryptonite folder
   ```
    python setup.py install
   ```
2. Save moeyex folder in the location below
   - \volatility3\volatility3\plugins\
3. Run moeyex plugin
   ```
   python vol.py moeyex --file-path=<file-path> --passphrase=<wallet-password>
   ```

# Decrypt wallet keys file
The wallet keys file encrypts and stores key values and wallet-related setting data.

## Features
decrypt_keys_file.py extracts key data(Public/Private keys) and 49 wallet-related setting data.

The output data is as:

"key_data": {
    "creation timestamp", "spend public key", "view public key", "encryption iv", "spend secret key", "view secret key"
},
  
"seed_language", "key_on_device", "watch_only", "multisig", "multisig_threshold", "always_confirm_transfers", "print_ring_members", "store_tx_info", "default_mixin", "default_priority", "auto_refresh", "refresh_type", "refresh_height", "skip_to_height", "confirm_non_default_ring_size", "ask_password", "max_reorg_depth", "min_output_count", "min_output_value", "default_decimal_point", "merge_destinations", "confirm_backlog", "confirm_backlog_threshold",
"confirm_export_overwrite", "auto_low_priority", "nettype", "segregate_pre_fork_outputs", "key_reuse_mitigation2", "segregation_height", "ignore_fractional_outputs", "ignore_outputs_above", "ignore_outputs_below", "track_uses", "background_sync_type", "show_wallet_name_when_locked", "inactivity_lock_timeout", "setup_background_mining", "subaddress_lookahead_major", "subaddress_lookahead_minor", "original_keys_available", "export_format", "load_deprecated_formats", "encrypted_secret_keys", "device_name", "device_derivation_path", "persistent_rpc_client_id", "auto_mine_for_rpc_payment", "credits_target", "enable_multisig"

## Use instructions
1. py-cryptonight install
   - Run cmd in the py-cryptonite folder
   ```
    python setup.py install
   ```
2. Run decrypt_keys_file.py
   ```
    python decrypt_keys_file.py --file=<file-path> --password=<wallet-password>
   ```

# Decrypt wallet cache file
The wallet cache file encrypts and stores transactions data related to imcoming, outgoing.

(The code can be decrypted for wallets that do not have an unconfirmed transaction and do not use subaddress and multisignature)

## Features
decrypt_wallet_file.py extracts transactions data.

The output data is as:

Type, Timestamp, BlockHeight, TX ID, TX Key, Amount, Fee, Change, Destination Address

## Use instructions
1. py-cryptonight install
   - Run cmd in the py-cryptonite folder
   ```
    python setup.py install
   ```
2. Run decrypt_cache_file.py
   ```
   python decrypt_cache_file.py --file=<file-path> --password=<wallet-password>
   ```

# Notice: Modified Third-Party Code
This repository includes code adapted from the py-cryptonight project.
Original repository: https://github.com/ph4r05/py-cryptonight
