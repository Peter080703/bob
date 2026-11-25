# Node Providers

## Conduit

Follow [Conduit's guide](https://docs.conduit.xyz/guides/run-a-node/op-stack-node) to run your own BOB node. Search "BOB" on their [Browse rollups page](https://app.conduit.xyz/browse-networks) and click "Run a node" to get started.

**Supported Networks**

- BOB Mainnet

## Tenderly

[Tenderly Node](https://tenderly.co/web3-gateway) provides a fast and reliable hosted node solution with a built-in suite of developer tooling and infrastructure building blocks covering your whole development lifecycle. Develop, test, deploy, and monitor your app on BOB with their [free and paid plans](https://tenderly.co/pricing).

**Supported Networks**

- [BOB Mainnet](https://bob.gateway.tenderly.co)

## dRPC

[dRPC](https://drpc.org/?utm_source=docs&utm_medium=bob) provides geo-distributed and auto-scalable RPC nodes that enhances security, reliability, and cost-efficiency for Web3 companies of all sizes. dRPC also supports Websockets.

**Supported Networks**

- [BOB Mainnet](https://drpc.org/chainlist/bob?utm_source=docs&utm_medium=bob)
- [BOB Sepolia](https://drpc.org/chainlist/bob?utm_source=docs&utm_medium=bob#bob-testnet) (Testnet)

## BoltRPC

[BoltRPC](https://boltrpc.io/networks/bob) is a multi-chain RPC provider operated by [Matrixed.Link](https://matrixed.link). BOB Mainnet is served over HTTPS and WebSocket with debug methods. Operations are ISO/IEC 27001:2022 certified.

**Supported Networks**

- [BOB Mainnet](https://boltrpc.io/networks/bob)

## Verify your RPC endpoint

Use the [Chain.Love BOB API directory](https://bob.chain.love/toolbox/apis) to
compare available hosted plans. Check your provider's documentation for the
supported networks, request limits, and historical data your app needs.

Before switching your app to a new endpoint, run this read-only check. Replace
the example URL with the endpoint your app will use.

```shell
curl --fail-with-body --silent --show-error --max-time 10 \
  -H 'Content-Type: application/json' \
  --data '{"jsonrpc":"2.0","id":1,"method":"eth_chainId","params":[]}' \
  https://rpc.gobob.xyz/
```

Expect `0xed88` (60808) for BOB Mainnet and `0xc576d` (808813) for BOB Sepolia.
These chain IDs are listed on the [Networks page](../user-hub/networks.md).
