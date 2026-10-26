<!-- gully-header:start -->
<a href="https://gullylabs.xyz"><img src="https://gullychain.xyz/brand/gully-labs/SimpleWebAuthn.svg" alt="Gully Labs · Gully ID: WebAuthn" width="100%"></a>

<p align="center">
  <a href="https://gullylabs.xyz"><img src="https://img.shields.io/badge/gullylabs.xyz-00D2FF?style=for-the-badge&labelColor=06050D&logo=googlechrome&logoColor=06050D" alt="Website"></a>
  <a href="https://docs.gullylabs.xyz"><img src="https://img.shields.io/badge/Docs-0B0A16?style=for-the-badge&labelColor=06050D&logo=readthedocs&logoColor=00D2FF" alt="Docs"></a>
  <a href="https://x.com/Gully_Labs"><img src="https://img.shields.io/badge/@Gully__Labs-0B0A16?style=for-the-badge&labelColor=06050D&logo=x&logoColor=white" alt="X"></a>
  <a href="https://t.me/GullyLabsNews"><img src="https://img.shields.io/badge/Telegram-0B0A16?style=for-the-badge&labelColor=06050D&logo=telegram&logoColor=26A5E4" alt="Telegram"></a>
  <a href="https://github.com/gully-labs"><img src="https://img.shields.io/badge/GitHub-0B0A16?style=for-the-badge&labelColor=06050D&logo=github&logoColor=white" alt="GitHub"></a>
</p>

<p align="center"><b>Gully ID: WebAuthn: SimpleWebAuthn, the passkey libraries used by Gully ID.</b></p>

<p align="center"><sub>Maintained by <a href="https://gullylabs.xyz">Gully Labs</a>. Fork of <a href="https://github.com/MasterKale/SimpleWebAuthn">MasterKale/SimpleWebAuthn</a>, used under its MIT licence. Not affiliated with or endorsed by Matthew Miller.</sub></p>

---
<!-- gully-header:end -->

# SimpleWebAuthn <!-- omit in toc -->

![WebAuthn](https://img.shields.io/badge/WebAuthn-Simplified-blueviolet?style=for-the-badge&logo=WebAuthn)
[![npm (scoped)](https://img.shields.io/npm/v/@simplewebauthn/server?style=for-the-badge&logo=npm)](https://www.npmjs.com/search?q=simplewebauthn)
[![JSR Scope](https://jsr.io/badges/@simplewebauthn?style=for-the-badge)](https://jsr.io/@simplewebauthn)

- [Overview](#overview)
- [Installation](#installation)
- [Documentation](#documentation)
- [Sponsors](#sponsors)
- [Example](#example)
- [Contributions](#contributions)
- [Development](#development)

## Overview

This project features two complimentary libraries to help reduce the amount of work needed to
incorporate WebAuthn into a website. The following packages are maintained here:

- [@simplewebauthn/server](https://github.com/MasterKale/SimpleWebAuthn/tree/master/packages/server)
- [@simplewebauthn/browser](https://github.com/MasterKale/SimpleWebAuthn/tree/master/packages/browser)

## Installation

SimpleWebAuthn can be installed from **[NPM](https://www.npmjs.com/search?q=%40simplewebauthn)** and
**[JSR](https://jsr.io/@simplewebauthn)** in **Node LTS 22.x and higher**, **Deno v2.4.x and
higher** projects, and other compatible runtimes (Cloudflare Workers, Bun, etc...)

See the packages' READMEs for more specific installation information.

### Supported Versions Strategy <!-- omit in toc -->

SimpleWebAuthn actively supports the following runtimes, targeting versions using the guidelines
below:

**Node:** LTS releases in Active and Maintenance mode, as per
https://nodejs.org/en/about/previous-releases.

**Deno:** SemVer minor releases (e.g. `2.4.x`) for up to one year after their release, as per
https://github.com/denoland/deno/releases.

## Documentation

In-depth documentation for this project is available at https://simplewebauthn.dev/docs

## Sponsors

Thank you very much to those who sponsor my work. Your contributions help keep the open-source dream
alive 🙇‍♂️

Interested in sponsoring this project? See here for more info:
https://github.com/sponsors/MasterKale

### 🌟 Platinum Sponsor <!-- omit from toc -->

<p class="sponsor-logo">
  <a href="https://a0.to/signup/simplewebauthn">
    <img src="https://github.com/user-attachments/assets/82bd296f-81c9-455f-b561-29119bd941c3" width="270" height="101" alt="Auth0 by Okta" />
    <br />
    <em>Simple Authentication. Make login our problem. Not yours.</em>
  </a>
</p>

### 🏅 Gold Sponsor <!-- omit from toc -->

<p class="sponsor-logo">
  <a href="https://www.authsignal.com">
    <img src="https://github.com/user-attachments/assets/475e8759-bb1a-4614-b3f9-b38002b11f34" width="270" height="63" alt="Authsignal" />
    <br />
    <em>Simple, drop-in passkeys and MFA as a Service</em>
  </a>
</p>

## Example

For a practical guide to implementing these libraries, take a look at the
[example project](https://github.com/MasterKale/SimpleWebAuthn/tree/master/example). It includes a
single-file Express server and a few HTML files that, combined with the packages in this repo, are
close to all it takes to get up and running with WebAuthn.

## Contributions

The SimpleWebAuthn project is not currently open to external contributions.

Please [submit an Issue](https://github.com/MasterKale/SimpleWebAuthn/issues/new/choose) and fill
out the provided template with as much information as possible if you have found a bug in need of
fixing.

You can also [submit an Issue](https://github.com/MasterKale/SimpleWebAuthn/issues/new/choose) to
request new features, or to suggest changes to existing features.

## Development

Install the following before proceeding:

- **Deno v2.4.x**

After pulling down the code, set up dependencies:

```sh
deno install
```

To run unit tests for all workspace packages, use the `test` series of scripts:

```sh
cd packages/browser/ && deno task test
```

```sh
cd packages/server/ && deno task test
```

Tests can be run in watch mode with the `test:watch` series of scripts:

```sh
cd packages/browser/ && deno task test:watch
```

```sh
cd packages/server/ && deno task test:watch
```

### Test Coverage <!-- omit in toc -->

The following additional dependencies are needed locally to display test coverage reports:

- **genhtml** (run `brew install lcov` on macOS to install this CLI tool)

Then run the following command to run tests and then host a coverage report at
http://127.0.0.1:8000:

```
deno run test:coverage
```
