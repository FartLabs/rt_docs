---
title: Getting started
---

Get started

# Intro

1\. [Install Deno](https://docs.deno.com/runtime/manual).

2\. Start a new Deno project.

```sh
deno init
```

3\. Add rt as a project dependency.

```sh
deno add jsr:@fartlabs/rt
```

# Use Example

```ts
import { Router } from "@fartlabs/rt";

const router = new Router()
  .get("/", () => new Response("Hello, World!"))
  .default(() => new Response("Not found", { status: 404 }));

Deno.serve((request) => router.fetch(request));
```
