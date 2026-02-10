# VerifyResultVerified

## Example Usage

```typescript
import { VerifyResultVerified } from "@vaibot/sdk/models";

let value: VerifyResultVerified = {
  ok: true,
  verified: true,
  contentHash: "<value>",
  agent: "<value>",
  timestamp: 844050,
  chain: "<value>",
  contractAddress: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        | Example            |
| ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| `ok`               | *boolean*          | :heavy_check_mark: | N/A                | true               |
| `verified`         | *boolean*          | :heavy_check_mark: | N/A                | true               |
| `contentHash`      | *string*           | :heavy_check_mark: | N/A                |                    |
| `agent`            | *string*           | :heavy_check_mark: | N/A                |                    |
| `timestamp`        | *number*           | :heavy_check_mark: | N/A                |                    |
| `chain`            | *string*           | :heavy_check_mark: | N/A                |                    |
| `contractAddress`  | *string*           | :heavy_check_mark: | N/A                |                    |