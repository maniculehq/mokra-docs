# Mokra Documentation

Official documentation for [Mokra](https://mokra.ai) — Mock servers for 800+ APIs. MockWorld Tests for AI agents.

## What is Mokra?

Mokra provides two products for developers:

### Mock Servers
Ready-to-go mock servers for 800+ real-world APIs. One credential. Realistic, stateful responses.

```ruby
# One API key for Stripe, Shopify, SendGrid, and 800+ more
charge = Stripe::Charge.create(amount: 5000, currency: "usd")
# => Returns realistic mock response
```

### MockWorld Tests
A testing framework for AI agents. Assert on outcomes, not reasoning paths. Implements the MockWorld Test paradigm introduced by Peter Nsaka.

```python
world = mockworld("Refund test", services=["stripe", "shopify"])

with world.run():
    agent.invoke("Process refund for order #1234")

world.observe()  # See what happened
world.assert("exactly one refund was created")  # Verify outcomes
```

## Documentation Structure

```
/
├── index.mdx                  # Homepage
├── mock-servers/              # Mock Servers documentation
├── mockworld-tests/           # MockWorld Tests documentation
├── guides/                    # Audience-specific guides
│   ├── api-integrations       # For traditional developers
│   ├── ai-code-generation     # For self-correcting AI
│   └── ai-agents              # For autonomous agents
├── services/                  # Service-specific docs (Stripe, Shopify, etc.)
├── sdks/                      # Ruby, Python, TypeScript SDKs
└── api-reference/             # HTTP API documentation
```

## Local Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

Run the local preview:

```bash
mint dev
```

View at `http://localhost:3000`

## Publishing

Changes pushed to the `main` branch are automatically deployed via the Mintlify GitHub app.

## Contributing

1. Create a branch for your changes
2. Run `mint dev` to preview locally
3. Submit a pull request

## Links

- [Mokra Dashboard](https://app.mokra.ai)
- [Mokra Website](https://mokra.ai)
- [mockworld-ruby SDK](https://github.com/AginSquash/mockworld-ruby)
