You can find all changes on the Releases page here: https://github.com/b365tech/iso8583/releases

# Changelog

## [v1.4.0]

Syncs the fork with upstream's latest release.

- Based on upstream tag: [moov-io/iso8583@v0.26.2](https://github.com/moov-io/iso8583/releases/tag/v0.26.2), up from v0.26.0.
- **Security and robustness fixes for parsing untrusted input** that v1.3.0 lacks:
  - Unknown TLV lengths in composite fields are bounds-checked (#427).
  - A truncated unknown TLV value returns an error instead of panicking (#415/#416).
  - `Track3.SetBytes` returns its unpack error.
  - An invalid composite spec returns an error instead of panicking (#448).
- cronos already runs upstream v0.26.1, from its Dependabot security-alert fix. This release lets every service use the fork without losing those fixes.

## [v1.3.0]

Syncs the fork with upstream.

- Based on upstream tag: [moov-io/iso8583@v0.26.0](https://github.com/moov-io/iso8583/releases/tag/v0.26.0), up from v0.23.4. This is the upstream version `transactioncodec` is built and tested against.
- Brings in, among other upstream changes, `Message.UnsetPath` (the newer name for `UnsetFields`, which is kept as a deprecated alias). `transactioncodec` v1.75.0 uses it, so consumers that replace `moov-io/iso8583` with this fork, such as switchPayment, need this release.
- Does not include the `v1.2.0` tag, which lives only on the `temp/track2bcd` branch (a Track 2 BCD encoder that `transactioncodec` provides itself in `moov_extensions`).

## [v1.0.0]

Initial release of the Banc365 fork.

- Based on upstream tag: [moov-io/iso8583@v0.23.4](https://github.com/moov-io/iso8583/releases/tag/v0.23.4)