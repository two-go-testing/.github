# two-go

Zero-dependency fluent service/API testing for Node.

**two-go** lets you build an HTTP request with a chainable API, attach the
checks you care about, and `await` it. No test runner required — works
standalone or inside node:test, Jest, Vitest, and Mocha.

## Repositories

- **[two-go](https://github.com/two-go-testing/two-go)** — the core library
  (HTTP client, assertions, schema validation, MCP server, and more).
- **[two-go-examples](https://github.com/two-go-testing/two-go-examples)** —
  runnable end-to-end examples (BDD shop suite, Docker Compose microservice).

## Quick start

```js
import { go } from "two-go";

await go("https://api.example.com")
  .get("/users")
  .bearer(token)
  .expectStatus(200)
  .expectJson("data[0].id", 1);
```

```bash
npm install two-go
```

MIT licensed · maintained by [@tugkanboz](https://github.com/tugkanboz)
