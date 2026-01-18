# Master of Arb v0.1.7
- Support copying notarb walelts that use up to four tokens.
- Preparations for multi-hop instructions support.
- Fixed an issue where three token instruction would cause incredibly high fees.
- Fixed an issue with notarb copy engine, wher the fees would not be updated dynamically
- Fixed an issue where the copy engine never starts again one the pipeline has been marked stale

# Master of Arb v0.1.6
- Switched some of the metrics like TX density to use the data from pools instead of tokens.
- Reworked pool selection.
- Added a "US Oil Reserve" token mint to blacklist.
- Fixed issue when some `raydium_amm_v4` pools were missing.
- Reworked & optimized pool search to no longer use specific `get_program_accounts_v2()` address. `HELIUS_API_KEY` is no longer required.
- Added `prefer_single_token` configuration option for assist. When enabled, it will always prefer sending for a single token given that there are enough pools.
- Added a check to make sure `min_priority_fee` & `max_priority_fee` does not exceed a maximum of 50,000 lamports.

# Master of Arb v0.1.5
- Fixed the running arbitrage copy with notarb engine.

# Master of Arb v0.1.4
- Added a `discovery_interval_seconds` setting for arbitrage assist.
- Changed wording for some of the messages.

# Master of Arb v0.1.3

- Included a `score_threshold` setting inside master.toml for custom strategies.
