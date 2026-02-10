# VerifyResultNotVerified

## Example Usage

```typescript
import { VerifyResultNotVerified } from "@vaibot/sdk/models";

let value: VerifyResultNotVerified = {
  ok: true,
  verified: false,
  contentHash: "<value>",
  chain: "<value>",
  contractAddress: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        | Example            |
| ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| `ok`               | *boolean*          | :heavy_check_mark: | N/A                | true               |
| `verified`         | *boolean*          | :heavy_check_mark: | N/A                | false              |
| `contentHash`      | *string*           | :heavy_check_mark: | N/A                |                    |
| `chain`            | *string*           | :heavy_check_mark: | N/A                |                    |
| `contractAddress`  | *string*           | :heavy_check_mark: | N/A                |                    |