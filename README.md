# SwapMatic API

SwapMatic API is a fork Uniswap API. It is a set of **authenticated** endpoints used by market aggregators (e.g. coinmarketcap.com) to surface 
Uniswap liquidity and volume information. All information is fetched from the underlying subgraphs.

The API is designed around the CoinMarketCap
[requirements document](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg).

Prefer the Uniswap subgraph for any Uniswap queries whenever possible. The respective subgraphs will always have more
recent data.

V1 Subgraph: https://github.com/graphprotocol/uniswap-subgraph

## Getting an API Key

Contact us [here](https://discord.gg/ZFr77Ra) if you would like to get an API key.

## Using an API Key

You can use an API key by setting it in the `x-api-key` header, like so:

```sh
curl -v --compressed https://api.swapmatic.io/v1/tickers -H 'x-api-key: abcd1234'
```

## V1 Documentation

The original Uniswap documentation of the `/v1/` endpoints is [here](./v1.md).

## Deploying the API

The API uses the [serverless framework](https://serverless.com) and can easily be deployed to any AWS account,
via the `yarn sls deploy` command.

In order to configure your AWS account as a target, 
see [the serverless docs](https://www.serverless.com/framework/docs/providers/aws/guide/credentials/).
