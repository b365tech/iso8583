You can find all changes on the Releases page here: https://github.com/b365tech/iso8583/releases

# Changelog

## [v1.3.0]

Syncs the fork with upstream.

- Based on upstream tag: [moov-io/iso8583@v0.26.0](https://github.com/moov-io/iso8583/releases/tag/v0.26.0), up from v0.23.4. This is the upstream version `transactioncodec` is built and tested against.
- Brings in, among other upstream changes, `Message.UnsetPath` (the newer name for `UnsetFields`, which is kept as a deprecated alias). `transactioncodec` v1.75.0 uses it, so consumers that replace `moov-io/iso8583` with this fork, such as switchPayment, need this release.
- Does not include the `v1.2.0` tag, which lives only on the `temp/track2bcd` branch (a Track 2 BCD encoder that `transactioncodec` provides itself in `moov_extensions`).

## [v1.0.0]

Initial release of the Banc365 fork.

- Based on upstream tag: [moov-io/iso8583@v0.23.4](https://github.com/moov-io/iso8583/releases/tag/v0.23.4)