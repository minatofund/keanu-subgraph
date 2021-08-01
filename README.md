# KEANU Subgraph
A subgraph of NuCypher(NU), KEEP and TBTC token on Ethereum mainnet 

## Deploy on Explorer
This subgraph has been deployed. You can find the details and use playground here.

https://thegraph.com/legacy-explorer/subgraph/minatofund/keanu-subgraph?selected=playground

## Demo
* Video Demo 

[https://youtu.be/QA0rAyanUtI](https://youtu.be/QA0rAyanUtI)

* Live Demo (Staging)

[https://knowyourdefistg.z11.web.core.windows.net/](https://knowyourdefistg.z11.web.core.windows.net/)

## Sample Query

```
{
  accounts(first: 5) {
    id
    totalSupply
    nuBalance
    keepBalance
    tbtcBalance
  }
  transferEvents(first: 5) {
    transaction {
      id
    }
    from
    to
    amount
    tokenType
  }
}
```

Response
```
{
  "data": {
    "accounts": [
      {
        "id": "0x0000000000000000000000000000000000000000",
        "keepBalance": "999848780.8",
        "nuBalance": "3885390081.748248632541961138",
        "tbtcBalance": "864.89",
        "totalSupply": true
      },
      {
        "id": "0x000000000000000000000000000000000000dead",
        "keepBalance": "0.000057213981223313",
        "nuBalance": "0",
        "tbtcBalance": "0.000000000000000008",
        "totalSupply": false
      },
      {
        "id": "0x000000000000006f6502b7f2bbac8c30a3f67e9a",
        "keepBalance": "0",
        "nuBalance": "0",
        "tbtcBalance": "0",
        "totalSupply": false
      },
      {
        "id": "0x000000000000084e91743124a982076c59f10084",
        "keepBalance": "0",
        "nuBalance": "0.000000000000000001",
        "tbtcBalance": "0",
        "totalSupply": false
      },
      {
        "id": "0x0000000000000eb4ec62758aae93400b3e5f7f18",
        "keepBalance": "0",
        "nuBalance": "0",
        "tbtcBalance": "0",
        "totalSupply": false
      }
    ],
    "transferEvents": [
      {
        "amount": "20213.12028179755583212",
        "from": "0xe6f19dab7d43317344282f803f8e8d240708174a",
        "to": "0xa356867fdcea8e71aeaf87805808803806231fdc",
        "tokenType": "KEEP",
        "transaction": {
          "id": "0x000040bcf042a3c333fd0eb358b224ae802954f888aef36bd5f29ee7ef05b694"
        }
      },
      {
        "amount": "20213.12028179755583212",
        "from": "0xa356867fdcea8e71aeaf87805808803806231fdc",
        "to": "0xc4b1a2de99870dd42cc3150080e6e3ae9bc5aa48",
        "tokenType": "KEEP",
        "transaction": {
          "id": "0x000040bcf042a3c333fd0eb358b224ae802954f888aef36bd5f29ee7ef05b694"
        }
      },
      {
        "amount": "117.99591476042445325",
        "from": "0xe6f19dab7d43317344282f803f8e8d240708174a",
        "to": "0x74de5d4fcbf63e00296fd95d33236b9794016631",
        "tokenType": "KEEP",
        "transaction": {
          "id": "0x000087248cbb8e9647eee528742d2cbf9f4f9e06b502309e0d054cbddbeab932"
        }
      },
      {
        "amount": "117.99591476042445325",
        "from": "0x74de5d4fcbf63e00296fd95d33236b9794016631",
        "to": "0xfc715223bfb7054955af0a1f8f4fc817e6abc3df",
        "tokenType": "KEEP",
        "transaction": {
          "id": "0x000087248cbb8e9647eee528742d2cbf9f4f9e06b502309e0d054cbddbeab932"
        }
      },
      {
        "amount": "20113.59",
        "from": "0xc78bf68570f6b9083e5fd2cb4257933730a168d8",
        "to": "0x28c6c06298d514db089934071355e5743bf21d60",
        "tokenType": "NU",
        "transaction": {
          "id": "0x0000b615701b98370fd102840ab90bd8f1898d4a73b3ed602b07a394bed98e4a"
        }
      }
    ]
  }
}
```
