<a href="http://ldap-passwords.com/">
<h1 align="center">Ldap-sha</h1>
</a>
<p align="center">Ldap SSHA password generator for node</p>
<p align="center">
   <a href="https://www.npmjs.com/package/ldap-sha">
      <img src="https://img.shields.io/npm/dt/ldap-sha?color=%23c12127&label=downloads&logo=npm" alt="npm"/>
   </a>
   <a href="https://github.com/dethdkn/ldap-sha/blob/main/LICENSE">
      <img src="https://img.shields.io/github/license/dethdkn/ldap-sha?color=%233da639&logo=open%20source%20initiative" alt="License"/>
  </a>
   <a href="https://gitmoji.dev">
      <img src="https://img.shields.io/badge/gitmoji-%20😜%20😍-FFDD67" alt="Gitmoji"/>
   </a>
   <a href="https://rosa.dev.br">
      <img src="https://img.shields.io/badge/check me!-👻-F28AA9" alt="rosa.dev.br"/>
   </a>
</p>

## ✨ Features

- Encrypt a plain text password with the Ldap SSHA algorithm.
- Verify passwords encrypted with SSHA.
- No external dependencies.

## 🚀 Setup

1. Install with your favorite package manager:
   - **pnpm** : `pnpm i ldap-sha`
   - npm : `npm i ldap-sha`
   - yarn : `yarn add ldap-sha`
   - bun : `bun add ldap-sha`

2. Import the function into your project:
```ts
import { ssha, verifySSHA } from 'ldap-sha'
```

## ⚡️ Usage

1. Encrypt a plain text password using SSHA:
```ts
const encryptedPassword = ssha('mySuperSecretPassword')
// return {SSHA}sTIysPunEI4boe6OwgQO+/tRZao2OWJIbDMvY0g2UlM=
```

2. Validate your plain text password with a SSHA encrypted password:\
**The SSHA password can be either a single string or an array of strings. The plain text password will be compared to each SSHA password and the function will return true if any of them matches**
```ts
const isValid = verifySSHA('mySuperSecretPassword', arrayOfSSHAPasswords)
// return true or false
```

## 📝 License

Copyright © 2024 [Gabriel 'DethDKN' Rosa](https://github.com/dethdkn)\
This project is under [MIT license](https://github.com/dethdkn/ldap-sha/blob/main/LICENSE)
