# Usage

## Overview

### Available Operations

* [get](#get) - Usage and quota

## get

Usage and quota

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/usage" method="get" path="/usage" -->
```typescript
import { Vaibot } from "@vaibot/sdk";

const vaibot = new Vaibot({
  bearerAuth: process.env["VAIBOT_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await vaibot.usage.get();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { VaibotCore } from "@vaibot/sdk/core.js";
import { usageGet } from "@vaibot/sdk/funcs/usage-get.js";

// Use `VaibotCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const vaibot = new VaibotCore({
  bearerAuth: process.env["VAIBOT_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await usageGet(vaibot);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("usageGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.UsageResult](../../models/usage-result.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.VaibotDefaultError | 4XX, 5XX                  | \*/\*                     |