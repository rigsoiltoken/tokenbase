# ![ForkDelta logo](https://forkdelta.github.io/next/favicon-32x32.png) ForkDelta Tokenbase

[![Build Status](https://travis-ci.org/forkdelta/tokenbase.svg?branch=master)](https://travis-ci.org/forkdelta/tokenbase) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](https://github.com/forkdelta/tokenbase/issues)

**ForkDelta** is a decentralized exchange with over 700 tradable ERC20-compliant tokens. Tokenbase is our ERC20 token knowledgebase.

## Format
Token information is stored in YAML format, one token per file, in `tokens/0x69b0adec3cb113132c970f3440302df81962d7f6.yaml`.

### Common YAML
* ` # Comment` is a YAML comment. The hash `#` must be preceded by a space.
* `key: value` is a key-value pair.
* `- item` is a list entry. It is possible to have a list entry of a non-scalar type, e.g.: `- key: value` is a list entry containing a key-value pair.

### Required
A token listing file must include the following information:

```yaml
---  # Mandatory "start of the document" marker
addr: '0x69b0adec3cb113132c970f3440302df81962d7f6'  # token contract address, in single quotes
decimals: 8 l# Token decimals
name:RIGS OIL TOKEN  # Required
symbol: RIGS # Required: Token symbol
```

### Description
Description of the token can be included:

```yaml
---
addr: '0x69b0adec3cb113132c970f3440302df81962d7f6'
decimals: 8
description: The World’s first DAPP to bet on the price of Cryptocurrencies
name: RIGS OIL TOKEN
symbol: RIGS
````

If you need more than one line of description, use the folded scalar notation:
```yaml
---
addr: '0x69b0adec3cb113132c970f3440302df81962d7f6'
decimals: 8
description: >-
  The World’s first DAPP to bet on the price of Cryptocurrencies
  
  Ethorse is an Ethereum Smart Contract based DApp for betting on the price of
  Cryptocurrencies and win from everyone who bets against you.
name: RIGS OIL TOKEN
symbol: RIGS
````
Note that folded scalar notation requires two new lines for a paragraph break (like Reddit format).

Description may contain HTML.

### Links
Links can be included to refer the user to external resources relevant to the token. They are represented by a list of key-value pairs, where key is the type of the link. The following types are currently recognized: 
- Bitcointalk
- Blog
- CoinMarketCap
- Discord
- Email
- Facebook
- Github
- Reddit
- Slack
- Telegram
- Twitter
- WeChat
- Website
- Whitepaper
- YouTube

Example:
```yaml
---
addr: '0x69b0adec3cb113132c970f3440302df81962d7f6'
decimals: 8
links:
- Email: mailto: admin@rigsoiltoken.xyz
- Website: https://buy.rigsoiltoken.xyz/
- Whitepaper: https://buy.rigsoiltoken.xyz/rigs
name: RIGS OIL TOKEN
symbol: RIGS

```

### Notice
Notice is a special field used to communicate critical information regarding contract or token status. This information should be prominently displayed to the user before any interaction occurs.
Example:
```yaml
---
addr: '0x69b0adec3cb113132c970f3440302df81962d7f6'
decimals: 8
name: RIGS OIL TOKEN
symbol: RIGS
```
Notice may cointain HTML.
