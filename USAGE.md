<!-- Start SDK Example Usage [usage] -->
```typescript
import { Vaibot } from "@vaibot/sdk";

const vaibot = new Vaibot({
  bearerAuth: process.env["VAIBOT_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await vaibot.proofs.create({
    content: "<value>",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->