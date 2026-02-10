# ProveInput

## Example Usage

```typescript
import { ProveInput } from "@vaibot/sdk/models";

let value: ProveInput = {
  content: "<value>",
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `content`                                | *string*                                 | :heavy_check_mark:                       | N/A                                      |
| `contentType`                            | *string*                                 | :heavy_minus_sign:                       | MIME type                                |
| `encoding`                               | [models.Encoding](../models/encoding.md) | :heavy_minus_sign:                       | N/A                                      |
| `model`                                  | *string*                                 | :heavy_minus_sign:                       | N/A                                      |
| `metadata`                               | Record<string, *any*>                    | :heavy_minus_sign:                       | N/A                                      |
| `idempotencyKey`                         | *string*                                 | :heavy_minus_sign:                       | N/A                                      |