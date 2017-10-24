Bitcore Node monacocoin
============

A monacocoin full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to [monacocoin Core v0.12.1.x](https://github.com/monacocoinpay/monacocoin/tree/v0.12.1.x) for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

## Install

```bash
npm install -g bitcore-node-monacocoin
```

## Prerequisites

- monacocoin Core (v0.12.1.x) with support for additional indexing *(see above)*
- Node.js v0.10, v0.12, v4 or v5
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~20GB of disk storage
- ~1GB of RAM

## Configuration

Bitcore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your Bitcore Node.

```bash
bitcore-node-monacocoin create -d <monacocoin-data-dir> mynode
cd mynode
bitcore-node-monacocoin install <service>
bitcore-node-monacocoin install https://github.com/yourname/helloworld
bitcore-node-monacocoin start
```

This will create a directory with configuration files for your node and install the necessary dependencies.

Please note that [monacocoin Core v0.12.1.x](https://github.com/monacocoinpay/monacocoin/tree/v0.12.1.x) will be downloaded automatically. Once completed the monacocoind binary should be placed into the &lt;monacocoin-data-dir&gt; folder specified during node creation.

For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

## Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/monacocoinpay/insight-api-monacocoin/tree/master)
- [Insight UI](https://github.com/monacocoinpay/insight-ui-monacocoin/tree/master)
- [Bitcore Wallet Service](https://github.com/monacocoinpay/bitcore-wallet-service/tree/master)

## Documentation

- [Upgrade Notes](docs/upgrade.md)
- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Interface to Bitcoin Core
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Development Environment](docs/development.md) - Guide for setting up a development environment
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Release Process](docs/release.md) - Information about verifying a release and the release process.

## Contributing

Please send pull requests for bug fixes, code optimization, and ideas for improvement. For more information on how to contribute, please refer to our [CONTRIBUTING](https://github.com/bitpay/bitcore/blob/master/CONTRIBUTING.md) file.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore-node-monacocoin/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc.

- bitcoin: Copyright (c) 2009-2015 Bitcoin Core Developers (MIT License)
