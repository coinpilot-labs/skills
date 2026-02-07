## coinpilot.json format

Store credentials at `tmp/coinpilot.json`:

```
{
  "apiKey": "EXPERIMENTAL_API_KEY",
  "apiBaseUrl": "https://api.coinpilot.bot",
  "userId": "did:privy:...",
  "wallets": [
    {
      "index": 0,
      "address": "0x...",
      "privateKey": "0x...",
      "isPrimary": true
    },
    {
      "index": 1,
      "address": "0x...",
      "privateKey": "0x...",
      "isPrimary": false
    }
  ]
}
```

Rules:

- Exactly one primary wallet (`isPrimary: true`) and it must be `index: 0`.
- Include exactly 10 wallets total: 1 primary + 9 subwallets.
- Subwallets should use indexes `1-9`.
- `apiBaseUrl` is optional. When provided, it overrides the default Coinpilot API base URL and must include the scheme (e.g. `https://`).
