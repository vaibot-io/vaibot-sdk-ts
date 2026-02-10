# Status

## Example Usage

```typescript
import { Status } from "@vaibot/sdk/models";

let value: Status = "confirmed";
```

## Values

This is an open enum. Unrecognized values will be captured as the `Unrecognized<string>` branded type.

```typescript
"pending" | "confirmed" | Unrecognized<string>
```