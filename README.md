# BTC Parachain Specification

This repository includes the specification for a two-way bridge between Polkadot and Bitcoin.
The bridge implements Bitcoin-backed tokens on a [Polkadot parachain](https://medium.com/polkadot-network/polkadot-the-parachain-3808040a769a).
The concept of Bitcoin-backed tokens is based on [Cryptocurrency-backed Assets](https://www.xclaim.io/).

The specification consists of two parts:

1. [XCLAIM(BTC,DOT) Bitcoin-backed tokens ](./interbtc-spec): The protocols and functions required to issue and redeem tokens as well as management of vaults.
2. [BTC-Relay](./btcrelay-spec/): The component that is used to verify Bitcoin transactions on the Polkadot parachain.

## Specification Documents

### BTC Parachain

- [Website](https://interlay.gitlab.io/interbtc-spec)
- [PDF](https://interlay.gitlab.io/interbtc-spec/interbtc-spec.pdf)

### BTC-Relay

- [Website](https://interlay.gitlab.io/interbtc-spec/btcrelay-spec/)
- [PDF](https://interlay.gitlab.io/interbtc-spec/btcrelay-spec.pdf)

## Contributing

You can contribute to this project. The following instructions will get you started with a local development environment.

### Requirements

The project is built with [Sphinx](https://www.sphinx-doc.org/en/master/).
Install the requirements with ``pip install -r requirements.txt``.


### Autobuild

Change into either the [btcrelay-spec](./btcrelay-spec/) or [interbtc-spec](./interbtc-spec) folder to work on either of the two specifications.
To have Sphinx automatically detect changes to .rst files and serve the latest changes in the browser, run `autobuild.sh`. 


- interBTC will be served at [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- BTC-Relay will be served at [http://127.0.0.1:9000/](http://127.0.0.1:9000/)

### LaTeX

You will have to have the required LaTeX packages installed to build the LaTeX files and export the document to PDF.

You can then run ``latexbuild.sh [DOCUMENT]`` where the document is either ``interbtc-spec``, ``btcrelay-spec``, or blank. Blank builds both specifications.
