## wallets.json format

Store credentials at `tmp/wallets.json`:

```
{
  "apiKey": "EXPERIMENTAL_API_KEY",
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
