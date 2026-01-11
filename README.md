# @pezkuwi/vanitygen

A CLI vanity address generator for Pezkuwichain

> Forked from [@polkadot/vanitygen](https://github.com/polkadot-js/tools) and adapted for Pezkuwichain

## Installation

```bash
npm install -g @pezkuwi/vanitygen
```

or

```bash
yarn global add @pezkuwi/vanitygen
```

## Usage

```bash
pezkuwi-vanitygen --match cook13 --mnemonic --network pezkuwi --type sr25519
```

### Options

- `--match <pattern>` - The pattern to match at the start of the address
- `--mnemonic` - Generate using a mnemonic (slower but recoverable)
- `--network <network>` - Network prefix: bizinikiwi, pezkuwi, dicle, zagros (default: pezkuwi)
- `--type <type>` - Key type: sr25519 (default) or ed25519

### Examples

Generate an address starting with "Pez":
```bash
pezkuwi-vanitygen --match Pez
```

Generate with mnemonic (recoverable):
```bash
pezkuwi-vanitygen --match cook --mnemonic
```

Generate ed25519 key:
```bash
pezkuwi-vanitygen --match test --type ed25519
```

## Notes

When using the `--mnemonic` option, the generation will be very slow since it needs to generate mnemonics and then test the resulting outputs.

As with all other CLI utilities, `--help` will return a list of the available options.

## License

Apache-2.0
