# TI Preprocessor package test repository

This repository contains package manifests for TI Preprocessor end-to-end testing.
The manifests cover npm, NuGet, Maven, Gradle, Python, and Cargo.

## Known package-verdict case

- `pkg:npm/eicar@1.0.0` is the known package expected to return a verdict and
  artifact SHA-256 from the Partner API `/packages/bulk` endpoint.
- When a SHA-256 is returned, TI Preprocessor also requests File Metadata
  Service data for that package.

The other real packages provide clean or unknown control cases. Synthetic
packages remain in the manifests to verify that missing partner data is handled
without failing package inventory output.
