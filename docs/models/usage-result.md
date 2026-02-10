# UsageResult

## Example Usage

```typescript
import { UsageResult } from "@vaibot/sdk/models";

let value: UsageResult = {
  month: "<value>",
  quota: {
    monthly: 969133,
    used: 22518,
    remaining: 912097,
  },
};
```

## Fields

| Field                              | Type                               | Required                           | Description                        |
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| `month`                            | *string*                           | :heavy_check_mark:                 | N/A                                |
| `quota`                            | [models.Quota](../models/quota.md) | :heavy_check_mark:                 | N/A                                |