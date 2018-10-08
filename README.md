# WoonklyMask Browser Extension
[![Build Status](https://circleci.com/gh/MetaMask/metamask-extension.svg?style=shield&circle-token=a1ddcf3cd38e29267f254c9c59d556d513e3a1fd)](https://circleci.com/gh/MetaMask/metamask-extension) [![Coverage Status](https://coveralls.io/repos/github/MetaMask/metamask-extension/badge.svg?branch=master)](https://coveralls.io/github/MetaMask/metamask-extension?branch=master) [![Greenkeeper badge](https://badges.greenkeeper.io/MetaMask/metamask-extension.svg)](https://greenkeeper.io/) [![Stories in Ready](https://badge.waffle.io/MetaMask/metamask-extension.png?label=in%20progress&title=waffle.io)](https://waffle.io/MetaMask/metamask-extension)

## Support

If you're a user seeking support, [here is our support site](https://metamask.helpscoutdocs.com/).

## Introduction

[Mission Statement](./MISSION.md)

[Internal documentation](./docs#documentation)

## Developing Compatible Dapps

If you're a web dapp developer, we've got two types of guides for you:

### New Dapp Developers

- We recommend this [Learning Solidity](https://karl.tech/learning-solidity-part-1-deploy-a-contract/) tutorial series by Karl Floersch.
- We wrote a (slightly outdated now) gentle introduction on [Developing Dapps with Truffle and MetaMask](https://medium.com/metamask/developing-ethereum-dapps-with-truffle-and-metamask-aa8ad7e363ba).

### Current Dapp Developers

- If you have a Dapp, and you want to ensure compatibility, [here is our guide on building MetaMask-compatible Dapps](https://github.com/MetaMask/faq/blob/master/DEVELOPERS.md)

## Building locally

 - Install [Node.js](https://nodejs.org/en/) version 8.11.3 and npm version 6.1.0
   - If you are using [nvm](https://github.com/creationix/nvm#installation) (recommended) running `nvm use` will automatically choose the right node version for you.
   - Select npm 6.1.0: ```npm install -g npm@6.1.0```
 - Install dependencies: ```npm install```
 - Install gulp globally with `npm install -g gulp-cli`.
 - Build the project to the `./dist/` folder with `gulp build`.
 - Optionally, to rebuild on file changes, run `gulp dev`.
 - To package .zip files for distribution, run `gulp zip`, or run the full build & zip with `gulp dist`.

 Uncompressed builds can be found in `/dist`, compressed builds can be found in `/builds` once they're built.

## Contributing

You can read [our internal docs here](https://metamask.github.io/metamask-extension/).

You can re-generate the docs locally by running `npm run doc`, and contributors can update the hosted docs by running `npm run publish-docs`.

### Running Tests

Requires `mocha` installed. Run `npm install -g mocha`.

Then just run `npm test`.

You can also test with a continuously watching process, via `npm run watch`.

You can run the linter by itself with `gulp lint`.

## Architecture

[![Architecture Diagram](./docs/architecture.png)][1]

## Development

```bash
npm install
npm start
```

## Build for Publishing

```bash
npm run dist
```

#### Writing Browser Tests

To write tests that will be run in the browser using QUnit, add your test files to `test/integration/lib`.

## Content
* Technologies used
* SDK interaction
* Tour
* Faucet
* Exchange
* Tokens
* Send
* Sell
* Deposit
* Remove
* Orders Book
* Chart
* Trade history
* Web3 interface
* Gas function

## Technologies used

## SDK Interaction
Woonkly will be able to web pages to use their pages to distribute advertising along with Woonks Catching, this interaction can be used in any web page. Only Woonkly user can catch Woonks.

## Tour
In the Woonkly Mask's extension will appear a little introduction when installed, this introduction will show users  how to handle the browser extension and its parts.

## Faucet
Woonkly will provide free Woonks to users, this will enhance user's motivation investing in our project.

## Exchange
The WoonklyMask browser extension has an exchange where users may interact with traders to exchange coins with tokens.

## Tokens
All transactions of token completed and denied are shown in Token's section, users will be able to see the amount per transaction and its date.

## Send
Users can send tokens to a wallet, it is necessary to write down the amount of Woonks and Price, so it will appear total amount of Ether used. And expiration is also a requirement that has to be specified.

## Sell
Users need to specify the amount, price and expiration of transaction, so it could be done.

## Deposit
This section allows users to deposit Woonks to Woonkly's token to interact with traders in the decentralized exchange.

## Remove
This section allows users to remove  Woonks from Woonkly's token that is used to interact with traders in the decentralized exchange.

## Order's book
Users will be able to see all orders listed in Order's book section, along with info over orders made.

## Chart
This section contains a chart that shows current price of Woonk, the price on its opening and ending per block number. Also handles volume information, and opening and ending volume per block number.

## Trade history
All trading info will be displayed in this sections where its sections will show date of transaction, type of transaction, BID and total.

## Web3 Interface

## Gas function
Users can set GAS amount of running transactions or contract through Ethereum blockchain.


## Other Docs

- [How to add custom build to Chrome](./docs/add-to-chrome.md)
- [How to add custom build to Firefox](./docs/add-to-firefox.md)
- [How to develop a live-reloading UI](./docs/ui-dev-mode.md)
- [How to add a new translation to MetaMask](./docs/translating-guide.md)
- [Publishing Guide](./docs/publishing.md)
- [The MetaMask Team](./docs/team.md)
- [How to develop an in-browser mocked UI](./docs/ui-mock-mode.md)
- [How to live reload on local dependency changes](./docs/developing-on-deps.md)
- [How to add new networks to the Provider Menu](./docs/adding-new-networks.md)
- [How to manage notices that appear when the app starts up](./docs/notices.md)
- [How to port MetaMask to a new platform](./docs/porting_to_new_environment.md)
- [How to use the TREZOR emulator](./docs/trezor-emulator.md)
- [How to generate a visualization of this repository's development](./docs/development-visualization.md)

[1]: http://www.nomnoml.com/#view/%5B%3Cactor%3Euser%5D%0A%0A%5Bmetamask-ui%7C%0A%20%20%20%5Btools%7C%0A%20%20%20%20%20react%0A%20%20%20%20%20redux%0A%20%20%20%20%20thunk%0A%20%20%20%20%20ethUtils%0A%20%20%20%20%20jazzicon%0A%20%20%20%5D%0A%20%20%20%5Bcomponents%7C%0A%20%20%20%20%20app%0A%20%20%20%20%20account-detail%0A%20%20%20%20%20accounts%0A%20%20%20%20%20locked-screen%0A%20%20%20%20%20restore-vault%0A%20%20%20%20%20identicon%0A%20%20%20%20%20config%0A%20%20%20%20%20info%0A%20%20%20%5D%0A%20%20%20%5Breducers%7C%0A%20%20%20%20%20app%0A%20%20%20%20%20metamask%0A%20%20%20%20%20identities%0A%20%20%20%5D%0A%20%20%20%5Bactions%7C%0A%20%20%20%20%20%5BaccountManager%5D%0A%20%20%20%5D%0A%20%20%20%5Bcomponents%5D%3A-%3E%5Bactions%5D%0A%20%20%20%5Bactions%5D%3A-%3E%5Breducers%5D%0A%20%20%20%5Breducers%5D%3A-%3E%5Bcomponents%5D%0A%5D%0A%0A%5Bweb%20dapp%7C%0A%20%20%5Bui%20code%5D%0A%20%20%5Bweb3%5D%0A%20%20%5Bmetamask-inpage%5D%0A%20%20%0A%20%20%5B%3Cactor%3Eui%20developer%5D%0A%20%20%5Bui%20developer%5D-%3E%5Bui%20code%5D%0A%20%20%5Bui%20code%5D%3C-%3E%5Bweb3%5D%0A%20%20%5Bweb3%5D%3C-%3E%5Bmetamask-inpage%5D%0A%5D%0A%0A%5Bmetamask-background%7C%0A%20%20%5Bprovider-engine%5D%0A%20%20%5Bhooked%20wallet%20subprovider%5D%0A%20%20%5Bid%20store%5D%0A%20%20%0A%20%20%5Bprovider-engine%5D%3C-%3E%5Bhooked%20wallet%20subprovider%5D%0A%20%20%5Bhooked%20wallet%20subprovider%5D%3C-%3E%5Bid%20store%5D%0A%20%20%5Bconfig%20manager%7C%0A%20%20%20%20%5Brpc%20configuration%5D%0A%20%20%20%20%5Bencrypted%20keys%5D%0A%20%20%20%20%5Bwallet%20nicknames%5D%0A%20%20%5D%0A%20%20%0A%20%20%5Bprovider-engine%5D%3C-%5Bconfig%20manager%5D%0A%20%20%5Bid%20store%5D%3C-%3E%5Bconfig%20manager%5D%0A%5D%0A%0A%5Buser%5D%3C-%3E%5Bmetamask-ui%5D%0A%0A%5Buser%5D%3C%3A--%3A%3E%5Bweb%20dapp%5D%0A%0A%5Bmetamask-contentscript%7C%0A%20%20%5Bplugin%20restart%20detector%5D%0A%20%20%5Brpc%20passthrough%5D%0A%5D%0A%0A%5Brpc%20%7C%0A%20%20%5Bethereum%20blockchain%20%7C%0A%20%20%20%20%5Bcontracts%5D%0A%20%20%20%20%5Baccounts%5D%0A%20%20%5D%0A%5D%0A%0A%5Bweb%20dapp%5D%3C%3A--%3A%3E%5Bmetamask-contentscript%5D%0A%5Bmetamask-contentscript%5D%3C-%3E%5Bmetamask-background%5D%0A%5Bmetamask-background%5D%3C-%3E%5Bmetamask-ui%5D%0A%5Bmetamask-background%5D%3C-%3E%5Brpc%5D%0A
