# ProofResult

## Example Usage

```typescript
import { ProofResult } from "@vaibot/sdk/models";

let value: ProofResult = {
  ok: true,
  contentHash: "<value>",
  agentAddress: "<value>",
  signature: "<value>",
  chainId: 921236,
  registry: "<value>",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          | Example                              |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `ok`                                 | *boolean*                            | :heavy_check_mark:                   | N/A                                  | true                                 |
| `txHash`                             | *string*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `contentHash`                        | *string*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `agentAddress`                       | *string*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `signature`                          | *string*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `chainId`                            | *number*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `registry`                           | *string*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `publisher`                          | *string*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `status`                             | [models.Status](../models/status.md) | :heavy_minus_sign:                   | N/A                                  |                                      |
| `url`                                | *string*                             | :heavy_minus_sign:                   | N/A                                  |                                      |