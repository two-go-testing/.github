# two-go

Zero-dependency fluent service/API testing for Node.

**two-go** lets you build an HTTP request with a chainable API, attach the
checks you care about, and `await` it. No test runner required. It works
standalone or inside node:test, Jest, Vitest, and Mocha.

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

## Repositories

- **[Two-Go](https://github.com/two-go-testing/two-go)** is the core library:
  HTTP client, assertions, schema validation, an optional AI layer, and an MCP
  server so agents can drive it.
- **[two-go-examples](https://github.com/two-go-testing/two-go-examples)** holds
  runnable end-to-end examples, including a BDD shop suite and a Docker Compose
  microservice tested against MySQL and MSSQL.
- **[two-go-docs](https://github.com/two-go-testing/two-go-docs)** is the
  documentation site.
- **[create-two-go](https://github.com/two-go-testing/create-two-go)** scaffolds
  a new test project with `npm create two-go`.
- **[two-go-action](https://github.com/two-go-testing/two-go-action)** is a
  GitHub Action that installs dependencies and runs your two-go tests in CI.
- **[two-go-vscode](https://github.com/two-go-testing/two-go-vscode)** is a VS
  Code extension with snippets and helpers for writing two-go tests.

MIT licensed. Maintained by [@tugkanboz](https://github.com/tugkanboz).
