# rentadomain.sh MCP server

Rent a domain name by the month: find it, price it, read the lease terms. You approve the rent.

Renting only, we never sell. Ownership never transfers.

This repository holds the listing for the hosted server. The server itself runs at rentadomain.sh; there is nothing
to install.

## Connect

Endpoint (streamable HTTP, no sign in for the public tools):

```
https://rentadomain.sh/mcp
```

Claude Code:

```
claude mcp add --transport http rentadomain https://rentadomain.sh/mcp
```

Any other client: add a remote MCP server with the URL above. Setup for each assistant:
https://rentadomain.sh/for-agents

## Tools

| Tool | What it does |
|---|---|
| search_names | Lists the names for rent right now, each with its monthly price and term menu; pass the person's own words |
| get_name | One name: listed, rented or not held, the monthly price for 12, 6 and 1 month terms, the renewal floor and ceiling |
| get_lease_terms | The exact lease text for one name and term, with its version and sha256 |
| how_to_rent | The exact steps for the agent and its person, with every URL |
| start_rent | Starts a rent and returns an approval link for the person |
| get_rent_status | The state of a rent the agent started |

An agent finds and prices a name and starts the rent. Only the person verifies, signs and pays: renting takes a
passkey, an identity check and a card.

## Money

Terms of 1, 6 or 12 months, billed monthly. No refunds after activation. Cancelling stops the next term; it is not a
refund. Every price comes from the tools, never from this file.

## Links

- Names for rent: https://rentadomain.sh/names
- For agents: https://rentadomain.sh/for-agents
- The lease: https://rentadomain.sh/lease
- Official MCP registry name: sh.rentadomain/rentadomain
