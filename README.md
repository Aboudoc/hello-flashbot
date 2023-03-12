### Setup

```sh
npm install @types/node ts-node tslib typescript --save-dev
```

```sh
npm install @flashbots/ethers-provider-bundle
npm install ethers@^5.5.2
```

### Run

```sh
env $(cat .env) npx ts-node src/index.ts
```

### Note

Deployed contract (GOERLI): 0x04b10028affBB22Ae6d98efFFfAb2FEF18e65958

If the simulation returns the following error

```sh
imulation error: err: max fee per gas less than block base fee
```

You need to increase the `maxFeePerGas` in you tx. You submitted it with less than the `baseFee`, so nodes will reject it to mitigate DoS attacks.

If you use `provider.getFeeData`, you will get recommended fee suggestions.
