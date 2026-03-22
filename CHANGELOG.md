# Master of Arb 1.0.0-rc.1
- Added a "notarbv2native" engine, to send notarb instructions directly to the chain.
- Added custom lookups management, lookups manager TUI.
- Added a settings TUI. The app is fully configurable through the TUI, no additional file editing needed.
- Added an ability to generate or import private key. This key is encrypted and the password stored in user's OS keychain.
- Added an ability to filter arbitrage mimic wallets.
- Added an ability to open solscan/circular/gmgn using "o" button.
- Added pool details window for arbitrage discover.
- Added an ability to send a single test transaction.
- Added support for pancakeswap pools parsing & discovery.
- Added tracking for pipelines that use secondary fees.
- Increased the amount of discovered pools.
- Removed the smb and notarb engines in favour of their native counterparts.
- Removed licenses, added a fee of 3.75% on successful arbitrage transactions.
- Removed Shyfy GQL Api in favour of Bitquery. This is a temporary solution until I find something that works better.
- Fixed an issue where the highlighted token would change after discovery cycle.

# Master of Arb 0.2.6
- Manual controls for arbitrage mimic, you can select wallet and start/stop engine directly from TUI.
- Fixed various crashes & errors during transactions parsing.
- Fixed UI issues, remove unimplemented 5m data.
- Fixed the issue where transactions window would show multiple tokens for a success transaction.
- Fixed an issue where secondary fee recipient prevented from parsing transactions.
- UI shows only last hour metrics. This is to better reflect the current market conditions.
- Logs window is no longer selectable.

# Master of Arb 0.2.5
- Fixed an issue where the highlighted pool index would pesist after selecting another token.
- Fixed an issue where selected pools will linger after being removed by discovery cycle.
- Fixed an issue where the monitor would crash if encountering missing accounts.
- Fixed an issue where the engine would keep running after app suspended/terminated/crashed. ⚠️ SIGKILL will still leave orphaned process ⚠️
- Added "Sender config" selection to engine controls.
- The application now starts with a simple `master` command and then displays the options to select the mode.
- UI improvements.

# Master of Arb v 0.2.4
- Pre-filter pools wtih < $1000 liquidity using RPC. This reduces the stress for Geckoterimnal enrichment, allowing for fetching more pools.
- Increase the amount of pools found.

# Master of Arb v 0.2.3
- It's no longer required to pass the fee config in `master.toml` to run the bot.
- Renamed `min_spam_tip_lamports` and `max_spam_tip_lamports` to `min_vendor_tip_lamports` and `max_vendor_tip_lamports` respectively.
- Add config for `min_jito_tip_lamports` and `max_jito_tip_lamports`

# Master of Arb v 0.2.2
Fix the 5m volume on the token list. It should show compound volume in the pools.
Remove `--verbose` flag, filter pools by price change.
The `--ui` flag will be enabled by default.

# Master of Arb v 0.2.1
- Fix the pump amm pool scanner.
- Increase the pool list.
- Improve the performance of pool fetching.
- The Master Assist now requires `SHYFT_API_KEY` to be set.

# Master of Arb v 0.2.0
- Introduce the UI for Assist, Copy & Monitor.
- Arbitrage assist manual mode, when you can select pools and run the selected engine manually.

# Master of Arb v0.1.7
- Support copying notarb walelts that use up to four tokens.
- Preparations for multi-hop instructions support.
- Fixed an issue where three token instruction would cause incredibly high fees.
- Fixed an issue with notarb copy engine, wher the fees would not be updated dynamically.
- Fixed an issue where the copy engine never starts again one the pipeline has been marked stale.

# Master of Arb v0.1.6
- Switched some of the metrics like TX density to use the data from pools instead of token
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
