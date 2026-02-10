# Proofs

## Overview

### Available Operations

* [create](#create) - Prove (sign + register) AI output
* [verify](#verify) - Verify proof by id or hash

## create

Prove (sign + register) AI output

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/prove" method="post" path="/prove" -->
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

### Standalone function

The standalone function version of this method:

```typescript
import { VaibotCore } from "@vaibot/sdk/core.js";
import { proofsCreate } from "@vaibot/sdk/funcs/proofs-create.js";

// Use `VaibotCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const vaibot = new VaibotCore({
  bearerAuth: process.env["VAIBOT_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await proofsCreate(vaibot, {
    content: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("proofsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.ProveInput](../../models/prove-input.md)                                                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ProofResult](../../models/proof-result.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorResponse      | 400                       | application/json          |
| errors.VaibotDefaultError | 4XX, 5XX                  | \*/\*                     |

## verify

Verify proof by id or hash

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/verify" method="post" path="/verify" -->
```typescript
import { Vaibot } from "@vaibot/sdk";

const vaibot = new Vaibot({
  bearerAuth: process.env["VAIBOT_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await vaibot.proofs.verify({
    proofId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { VaibotCore } from "@vaibot/sdk/core.js";
import { proofsVerify } from "@vaibot/sdk/funcs/proofs-verify.js";

// Use `VaibotCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const vaibot = new VaibotCore({
  bearerAuth: process.env["VAIBOT_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await proofsVerify(vaibot, {
    proofId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("proofsVerify failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.VerifyRequestUnion](../../models/verify-request-union.md)                                                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostVerifyResponse](../../models/operations/post-verify-response.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorResponse      | 400                       | application/json          |
| errors.VaibotDefaultError | 4XX, 5XX                  | \*/\*                     |