# Build

Dependency management is done via [Glide](https://glide.sh).

```bash
glide install
go build
```


# API

## Stats

GET localhost:8080/api/cndy/stats[?from=2018-03-03T23:05:40Z&to=2018-03-03T23:05:50Z]

If not set, `from` defaults to UNIX timestamp `0`, `to` to `now`.

```json
{
  "accounts_involved": 3,
  "amount_transferred": 2119,
  "asset_code": "CNDY",
  "current_cursor": "33592975036518402-2",
  "trustlines_created": 1,
  "tx_count": 25
}
```

## Transactions

GET localhost:8080/api/cndy/transactions[?from=2018-03-03T23:05:40Z&to=2018-03-03T23:05:50Z]

If not set, `from` defaults to UNIX timestamp `0`, `to` to `now`.

```json
{
  "transactions": [
    {
      "id": "0033170775456358401-0000000001",
      "operation": "https://horizon-testnet.stellar.org/operations/33170775456358401",
      "paging_token": "33170775456358401-1",
      "account": "GDQLK4Y26S5H6X3WAAMKFIT2575N54B667TCJA3KTS5XBYL5KUJWMFRM",
      "amount": "12.0000000",
      "type": "account_credited",
      "starting_balance": "",
      "balance": "",
      "balance_limit": "",
      "asset_type": "credit_alphanum4",
      "asset_code": "CNDY",
      "asset_issuer": "GD7YB3R3TKUU3OHTE3DO5BIVBLQVFKYRHPW5Y6NHVSQVNNEOQ5I2RKLU",
      "created_at": "2018-03-03T23:05:43Z"
    },
    {
      "id": "0033170775456358401-0000000002",
      "operation": "https://horizon-testnet.stellar.org/operations/33170775456358401",
      "paging_token": "33170775456358401-2",
      "account": "GD7YB3R3TKUU3OHTE3DO5BIVBLQVFKYRHPW5Y6NHVSQVNNEOQ5I2RKLU",
      "amount": "12.0000000",
      "type": "account_debited",
      "starting_balance": "",
      "balance": "",
      "balance_limit": "",
      "asset_type": "credit_alphanum4",
      "asset_code": "CNDY",
      "asset_issuer": "GD7YB3R3TKUU3OHTE3DO5BIVBLQVFKYRHPW5Y6NHVSQVNNEOQ5I2RKLU",
      "created_at": "2018-03-03T23:05:43Z"
    }
  ]
}
```
