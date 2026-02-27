# /ape

Run full degen DD on a token. Pulls live on-chain data and returns a DEGEN SCORE + verdict.

## Usage
```
/ape [contract_address]
/ape [contract_address] [chain]
```

## Examples
```
/ape 3G36hCsP5DgDT2hGxACivRvzWeuX56mU9DrFibbKpump
/ape 0x1234...abcd eth
```

## What it does
Runs the `degen-dd` skill: snapshot, red flags, whale activity, social check, DEGEN SCORE verdict.
