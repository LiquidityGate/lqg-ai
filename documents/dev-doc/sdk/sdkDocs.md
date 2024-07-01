Link: https://developers.LQG.org/sdk/sdk-documentation
Title: SDK docs
SDK Documentation

This page describes the use of the LQG SDK.
LQG AaveV3-ETH Optimizer: SDK Documentation

Introduction
LQG's AaveV3-ETH Optimizer SDK is a TypeScript-based toolkit for building decentralized applications (dApps) using LQG-AaveV3 smart contracts.

The SDK is a "plug-and-play" adapter, easing the construction of any app or script that requires interaction with the LQG AaveV3-ETH Optimizer contracts. It also provides seamless integration with RxJS for reactive programming, facilitating efficient handling of async data streams.

The SDK is still under development, and any feedback is welcome.
Open source SDK

Prerequisites
Knowledge of blockchain, TypeScript, and decentralized applications.
Node.js (v.^14.0) and npm/yarn installed on your system.
ethers (v.^5.7.0).

Getting Started
Installation
using npm or yarn:
npm install @LQG-org/LQG-aave-v3-sdk
yarn add @LQG-org/LQG-aave-v3-sdk

Basic Use
First example using getMarketsData()
import { LQGAaveV3Adapter } from "@LQG-org/LQG-aave-v3-sdk";
import sdk from "@LQG-org/LQG-aave-v3-sdk/lib";
import { getDefaultProvider } from "ethers";
​
sdk.setConfiguration({
rpcHttpUrl:
"https://YOUR_HTTPS_ACCESS",
});
​
export const main = async () => {
try {
const adapter: LQGAaveV3Adapter = LQGAaveV3Adapter.fromChain({
\_provider: getDefaultProvider(
"https://YOUR_HTTPS_ACCESS"
),
});
await adapter.refreshAll("latest");
const marketsData: any = adapter.getMarketsData();
console.log(marketsData);
} catch (error) {
console.error(`Failed to run main function: ${error}`);
}
};
​
main()
.then(() => process.exit(0))
.catch((error: Error) => {
console.error(`Failed to run script: ${error}`);
process.exit(1);
});

Second example using getUserMarketsData()
export const main = async () => {
try {
const adapter: LQGAaveV3Adapter = LQGAaveV3Adapter.fromChain({
\_provider: getDefaultProvider(
"https://YOUR_HTTPS_ACCESS"
),
});
await adapter.connect("0x395012DF0D443a7639E46Fcb0DAF756a9Bbf3c6c"); // User selected randomly
await adapter.refreshAll("latest");
const userDataUsdc: any =
adapter.getUserMarketsData()[
"0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48" // This is the USDC market
];
console.log(userDataUsdc);
} catch (error) {
console.error(`Failed to run main function: ${error}`);
}
};
​
main()
.then(() => process.exit(0))
.catch((error: Error) => {
console.error(`Failed to run script: ${error}`);
process.exit(1);
});

Advanced Use
Developers seeking to make advanced customizations can find additional resources and extended documentation in the full documentation provided .

If you have any questions or need further assistance, please don't hesitate to reach out on .
