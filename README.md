# Arbitrage Assist

To run arbitrage assist you need to first populate the look up tables file:
```sh
master lookups populate
```

This will automatically generate 10 lookup tables, which then can be used to run the assist tool

Set the desired parameters in the `config/master.toml` file, then run:
```
master assist 
```

When opportunity found, the seed config `config/notarb_config.toml` will be used

## Environment Variables

Environment located in `.env` file:
```sh
touch .env
```

The following environment variables required to run:
```sh
HELIUS_API_KEY= # used to fetch the pools data
LICENSE_KEY= # valid license key to run the software
JSON_RPC_URL= # RPC url to connect to the Solana network
```

# Arbitrage copy
To run arbitrage copy you need to first select tracked wallet inside `config/master.toml`

After that you can run copy assits
```sh
master copy
# or
master copy --ui
```

## Environment Variables

Environment located in `.env` file:
```sh
touch .env
```

The following variables required to run:
```sh
LICENSE_KEY= # valid license key to run the software
JSON_RPC_URL= # RPC url to connect to the Solana network
```

# Engines

To run either SMB or Notarb, you have to put them into directory:
```sh
/engines/notarb
/engines/smb
```

Or you can specify custom directory using `config/master.toml`
